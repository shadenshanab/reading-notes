# class 26

## Permissions & Postgresql

--------------

* Permission checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the request.user and request.auth properties to determine if the incoming request should be permitted.

## How permissions are determined

* Permissions in REST framework are always defined as a list of permission classes.

Before running the main body of the view each permission in the list is checked. If any permission check fails, an exceptions.PermissionDenied or exceptions.NotAuthenticated exception will be raised, and the main body of the view will not run.

## Object level permissions

* REST framework permissions also support object-level permissioning. Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.

Object level permissions are run by REST framework's generic views when .get_object() is called. As with view level permissions, an exceptions.PermissionDenied exception will be raised if the user is not allowed to act on the given object.

If you're writing your own views and want to enforce object level permissions, or if you override the get_object method on a generic view, then you'll need to explicitly call the .check_object_permissions(request, obj) method on the view at the point at which you've retrieved the object.

For example:

def get_object(self):
    obj = get_object_or_404(self.get_queryset(), pk=self.kwargs["pk"])
    self.check_object_permissions(self.request, obj)
    return obj

#### Setting the permission policy

* he default permission policy may be set globally, using the DEFAULT_PERMISSION_CLASSES setting. For example.

REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}

### API Reference

* AllowAny:
The AllowAny permission class will allow unrestricted access, regardless of if the request was authenticated or unauthenticated.

* IsAuthenticated: The IsAuthenticated permission class will deny permission to any unauthenticated user, and allow permission otherwise.

This permission is suitable if you want your API to only be accessible to registered users.

* IsAdminUser : The IsAdminUser permission class will deny permission to any user, unless user.is_staff is True in which case permission will be allowed.

This permission is suitable if you want your API to only be accessible to a subset of trusted administrators

## Custom permissions

* To implement a custom permission, override BasePermission and implement either, or both, of the following methods:

.has_permission(self, request, view)
.has_object_permission(self, request, view, obj)

## Overview of access restriction methods

REST framework offers three different methods to customize access restrictions on a case-by-case basis. These apply in different scenarios and have different effects and limitations.

-queryset/get_queryset(): Limits the general visibility of existing objects from the database. The queryset limits which objects will be listed and which objects can be modified or deleted. The get_queryset() method can apply different querysets based on the current action.

-permission_classes/get_permissions(): General permission checks based on the current action, request and targeted object. Object level permissions can only be applied to retrieve, modify and deletion actions. Permission checks for list and create will be applied to the entire object type. (In case of list: subject to restrictions in the queryset.)

-serializer_class/get_serializer(): Instance level restrictions that apply to all objects on input and output. The serializer may have access to the request context. The get_serializer() method can apply different serializers based on the current action.
