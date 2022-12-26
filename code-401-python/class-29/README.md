# class 29

## API Deployment

--------------

## Configuring Django Settings: Best Practices

- Managing Django Settings: Issues
  
  - Different environments.

    Usually, you have several environments: local, dev, ci, qa, staging, production, etc. Each environment can have its own specific settings (for example: DEBUG = True, more verbose logging, additional apps, some mocked data, etc). You need an approach that allows you to keep all these Django setting configurations.

  - Sensitive data.

    You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This data cannot be stored in VCS.

  - Sharing settings between team members.

    You need a general approach to eliminate human error when working with the settings. For example, a developer may add a third-party app or some API integration and fail to add specific settings. On large (or even mid-size) projects, this can cause real issues.
  - Django settings are a Python code.

    This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem – instead of key-value pairs, settings.py can have a very tricky logic.

### Setting Django Configurations: Different Approaches

There is no built-in universal way to configure Django settings without hardcoding them. But books, open-source and work projects provide a lot of recommendations and approaches on how to do it best. Let’s take a brief look at the most popular ones to examine their weaknesses and strengths.

- settings_local.py

    This is the oldest method. I used it when I was configuring a Django project on a production server for the first time. I saw a lot of people use it back in the day, and I still see it now.

    The basic idea of this method is to extend all environment-specific settings in the settings_local.py file, which is ignored by VCS.
    Here’s an example:

**settings.py file:**

```python
   ALLOWED_HOSTS = ['example.com']
    DEBUG = False
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.postgresql',
            'NAME': 'production_db',
            'USER': 'user',
            'PASSWORD': 'password',
            'HOST': 'db.example.com',
            'PORT': '5432',
            'OPTIONS': {
                'sslmode': 'require'
            }
        }
    }

    ...

    from .settings_local import *
```

**settings_local.py file:**

```python
ALLOWED_HOSTS = ['localhost']
DEBUG = True
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'local_db',
        'HOST': '127.0.0.1',
        'PORT': '5432',
    }
}
```

#### Pros

- Secrets not in VCS.

#### Cons

- settings_local.py is not in VCS, so you can lose some of your Django environment settings.
- The Django settings file is a Python code, so settings_local.py can have some non-obvious logic.
- You need to have settings_local.example (in VCS) to share the default Django configurations for developers.

## What Is SSH: Understanding Encryption, Ports and Connection

### What Is SSH?

SSH, or Secure Shell Protocol, is a remote administration protocol that allows users to access, control, and modify their remote servers over the internet.

SSH service was created as a secure replacement for the unencrypted Telnet and uses cryptographic techniques to ensure that all communication to and from the remote server happens in an encrypted manner. It provides a mechanism for authenticating a remote user, transferring inputs from the client to the host, and relaying the output back to the client.

The example below shows a typical SSH prompt. Any Linux or macOS user can SSH into their remote server directly from the terminal window. Windows users can take advantage of SSH clients like Putty.  You can execute shell commands in the same manner as you would if you were physically operating the remote computer.

### How Does SSH Work

If you’re using Linux or Mac, then using SSH is very simple. If you use Windows, you will need to utilize an SSH client to open SSH connections. The most popular SSH client is PuTTY, which you can learn more about here.

For Mac and Linux users, head over to your terminal program and then follow the procedure below:

The SSH command consists of 3 distinct parts:

`ssh {user}@{host}`

The SSH key command instructs your system that you want to open an encrypted Secure Shell Connection. {user} represents the account you want to access. For example, you may want to access the root user, which is basically synonymous with the system administrator with complete rights to modify anything on the system. {host} refers to the computer you want to access. This can be an IP Address (e.g. 244.235.23.19) or a domain name (e.g. www.xyzdomain.com).

When you hit enter, you will be prompted to enter the password for the requested account. When you type it in, nothing will appear on the screen, but your password is, in fact being transmitted. Once you’re done typing, hit enter once again. If your password is correct, you will be greeted with a remote terminal window.

### Understanding Different Encryption Techniques

Understanding Different Encryption Techniques
The significant advantage offered by SSH over its predecessors is the use of encryption to ensure a secure transfer of information between the host and the client. Host refers to the remote server you are trying to access, while the client is the computer you are using to access the host. There are three different encryption technologies used by SSH:

1. Symmetrical encryption: Symmetric encryption is a form of encryption where a secret key is used for both encryption and decryption of a message by both the client and the host. Effectively, anyone possessing the key can decrypt the message being transferred.

2. Asymmetrical encryption: Unlike symmetrical encryption, asymmetrical encryption uses two separate keys for encryption and decryption. These two keys are known as the public key and the private key. Together, both these keys form a public-private key pair.

3. Hashing:One-way hashing is another form of cryptography used in Secure Shell Connections. One-way-hash functions differ from the above two forms of encryption in the sense that they are never meant to be decrypted. They generate a unique value of a fixed length for each input that shows no clear trend which can be exploited. This makes them practically impossible to reverse.
