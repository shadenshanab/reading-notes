# class 28

## Authentication & Production Server

--------------

## Introduction to JSON Web Tokens (JWTs)

- JSON Web Tokens (JWTs) are a standard for representing claims securely between two parties.
- JWTs consist of three parts: a header, a payload, and a signature.
- The header specifies the algorithm used to generate the signature.
- The payload contains the claims, which are statements about an entity (typically, the user) and additional data. Claims can be publicly visible or private.
- The signature is used to verify that the sender of the JWT is who it claims to be, and to ensure that the message wasn't changed along the way.
- JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.
- JWTs are often used to authenticate users in APIs. They can be stored in cookies, local storage, or sent as authorization headers.

## Using JWT Authentication with Django REST Framework

- Django REST framework provides built-in support for JWT authentication.
- To use JWT authentication, you will need to install the `djangorestframework-jwt` package and add it to your `INSTALLED_APPS`.
- In your Django settings, you will need to set the `JWT_AUTH` settings to specify the algorithm and secret used to sign JWTs.
- You can then use the `JWTAuthentication` class as the authentication class for your API views, or use the `@jwt_required` decorator on specific views or viewset methods that require authentication.
- To authenticate with a JWT, a client can send the JWT in the `Authorization` header with the `Bearer` scheme, or as a query string parameter.
- The `JWTAuthentication` class will authenticate the user and attach the user object to the request, which can be accessed in your views and serializers as `request.user`.
- You can also use the `JWTUserAuthentication` class, which will authenticate the user and set the `request.user` attribute to the user object, but will raise an exception if the user is not authenticated.
- You can use the `JSONWebTokenAuthentication` class as a more flexible alternative to `JWTAuthentication`, which allows you to specify the `HTTP_AUTHORIZATION_NAME` and `QUERY_PARAM` settings to customize how the JWT is passed to the server.
- You can use the `RefreshJSONWebToken` view to refresh an expired JWT by sending a `POST` request with a valid JWT in the `Authorization` header.
- You can also use the `ObtainJSONWebToken` view to obtain a JWT by sending a `POST` request with valid credentials.
- The `JWTDecodeError` and `ExpiredSignatureError` exceptions can be handled using Django's exception handling mechanism.
