# class 25

## Django REST Framework & Docker

--------------

**Docker** is a complex beast under the hood.

**Virtualization** has its roots at the beginning of computer science when large, expensive mainframe computers were the norm. virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.

**Virtual environments** are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.

## Install Docker

**Docker Compose** is an additional tool that is automatically included with Mac and Windows downloads of Docker. However if you are on Linux, you will need to add it manually. You can do this by running the command `sudo pip install docker-compose`

* To confirm Docker installed correctly we can run our first command `docker run hello-world`

## Django for APIs - Library Website

**Django REST Framework** works alongside the Django web framework to create web APIs. We cannot build a web **API** with only Django Rest Framework. It always must be added to a project after Django itself has been installed and configured.

The `.venv` directory was created with our virtual environment but Django has added a django_project directory and a manage.py file. Within django_project are five new files:

* `__init__.py` indicates that the files in the folder are part of a Python package. Without this file, we cannot import files from another directory which we will be doing a lot of in Django!
* `asgi.py` allows for an optional Asynchronous Server Gateway Interface to be run
* `settings.py` controls our Django project’s overall settings
* `urls.py` tells Django which pages to build in response to a browser or URL request
* `wsgi.py` stands for Web Server Gateway Interface which helps Django serve our eventual web pages.

### The important takeaways from this tutorial are this

1. Docker is a way to run Linux containers
2. Containers are a lightweight alternative to Virtual Machines
3. **Dockerfile** is a list of instructions for creating an image
4. Images are made up of one or more layers
5. Containers are a running instance of an image
6. **docker-compose.yml** controls how to run the container
7. Containers are stateless and ephemeral in nature. We can link the local filesystem via **volumes** but things become more complex with databases.
