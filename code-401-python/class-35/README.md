# class 35

## Authentication

--------------

### What is authentication?

Authentication is the process of determining whether someone or something is, in fact, who or what it says it is. Authentication technology provides access control for systems by checking to see if a user's credentials match the credentials in a database of authorized users or in a data authentication server. In doing this, authentication assures secure systems, secure processes and enterprise information security.

There are several authentication types. For purposes of user identity, users are typically identified with a user ID, and authentication occurs when the user provides credentials such as a password that matches their user ID. The practice of requiring a user ID and password is known as single-factor authentication (SFA). In recent years, companies have strengthened authentication by asking for additional authentication factors, such as a unique code that is provided to a user over a mobile device when a sign-on is attempted or a biometric signature, like a facial scan or thumbprint. This is known as two-factor authentication (2FA).

Authentication factors can even go further than SFA, which requires a user ID and password, or 2FA, which requires a user ID, password and biometric signature. When three or more identity verification factors are used for authentication -- for example, a user ID and password, biometric signature and perhaps a personal question the user must answer -- it is called multifactor authentication (MFA).

### Why is authentication important in cybersecurity?

Authentication enables organizations to keep their networks secure by permitting only authenticated users or processes to gain access to their protected resources. This may include computer systems, networks, databases, websites and other network-based applications or services.

Once authenticated, a user or process is usually subjected to an authorization process to determine whether the authenticated entity should be permitted access to a specific protected resource or system. A user can be authenticated but not be given access to a specific resource if that user was not granted permission to access it.

The terms authentication and authorization are often used interchangeably. While they are often implemented together, they are two distinct functions. Authentication is the process of validating the identity of a registered user or process before enabling access to protected networks and systems. Authorization is a more granular process that validates that the authenticated user or process has been granted permission to gain access to the specific resource that has been requested. The process by which access to those resources is restricted to a certain number of users is called access control. The authentication process always comes before the authorization process.

### How does authentication work?

During authentication, credentials provided by the user are compared to those on file in a database of authorized users' information either on the local operating system server or through an authentication server. If the credentials entered match those on file and the authenticated entity is authorized to use the resource, the user is granted access. User permissions determine which resources the user gains access to and also any other access rights that are linked to the user, such as during which hours the user can access the resource and how much of the resource the user is allowed to consume.

Traditionally, authentication was accomplished by the systems or resources being accessed. For example, a server would authenticate users using its own password system, login IDs, or usernames and passwords.

However, the web's application protocols -- Hypertext Transfer Protocol and HTTP Secure -- are stateless, meaning that strict authentication would require end users to reauthenticate each time they access a resource using HTTPS. To simplify user authentication for web applications, the authenticating system issues a signed authentication token to the end-user application; that token is appended to every request from the client. This means that users do not have to sign on every time they use a web application.

### What is authentication used for?

User and process authentication are used to ensure that only authorized individuals or processes are allowed to access company IT resources. Depending on the use cases for which authentication is used, authentication can consist of either SFA, 2FA or MFA.

The most common implementation of authentication is SFA, which requires a user ID and a password for sign-on and access. However, since banks and many companies now use online banking and e-commerce to conduct business and store customer Social Security and credit and debit card numbers, there is an increased use of 2FA and even MFA, which requires users and customers to enter not only a user ID and password, but also additional authentication information.
