# Virtual Environment, install Django and Create a project

- [Creating Virtual Environment](#Creating%20Virtual%20Environment)
- [Install Django](#Install%20Django)
- [Creating a project](#Creating%20a%20project)
- [The development server](#the%20development%20server)
- [The development server](#The%20development%20server)
	- [Automatic reloading of runserver](#Automatic%20reloading%20of%20runserver)
	- [Changing the port](#Changing%20the%20port)

## Creating Virtual Environment

Run the [venv](https://docs.python.org/3/library/venv.html#module-venv "venv: Creation of virtual environments.") module as a script in the directory path where you want to place it

``` sh
py -m venv <name-env>
```

Activate the virtual environment

``` sh
<name-env>\Scripts\activate.bat

or

cd .\<name-env>\Scripts\
.\activate
```

To deactivate the virtual environment, type

``` sh
deactivate
```

## Install Django

``` sh
py -m pip install Django
```

To verify that Django can be seen by Python, type `python` from your shell. Then at the Python prompt, try to import Django

``` sh
>>> import django
>>> print(django.get_version())
>>> quit()
```

You can also tell Django is installed and which version by running the following command in a shell prompt

``` sh
py -m django --version
```

## Creating a project

``` sh
django-admin startproject 'mysite'
python manage.py runserver
```

> [!note] 
> You’ll need to avoid naming projects after built-in Python or Django components. In particular, this means you should avoid using names like `django` (which will conflict with Django itself) or `test` (which conflicts with a built-in Python package) 

Let’s look at what [`startproject`](https://docs.djangoproject.com/en/4.2/ref/django-admin/#django-admin-startproject) created

``` 
mysite/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
```

These files are:

- The outer **mysite/** root directory is a container for your project. Its name doesn’t matter to Django; you can rename it to anything you like.
- **manage.py**: A command-line utility that lets you interact with this Django project in various ways. You can read all the details about *manage.py* in [django-admin and manage.py](https://docs.djangoproject.com/en/4.2/ref/django-admin/).
- The inner **mysite/** directory is the actual Python package for your project. Its name is the Python package name you’ll need to use to import anything inside it (e.g. *mysite.urls*).
- **__init__.py:** An empty file that tells Python that this directory should be considered a Python package. If you’re a Python beginner, read [more about packages](https://docs.python.org/3/tutorial/modules.html#tut-packages "(in Python v3.11)") in the official Python docs.
-  **settings.py**: Settings/configuration for this Django project. [Django settings](https://docs.djangoproject.com/en/4.2/topics/settings/) will tell you all about how settings work.
- **urls.py**: The URL declarations for this Django project; a “table of contents” of your Django-powered site. You can read more about URLs in [URL dispatcher](https://docs.djangoproject.com/en/4.2/topics/http/urls/).
- **asgi.py**: An entry-point for ASGI-compatible web servers to serve your project. See [How to deploy with ASGI](https://docs.djangoproject.com/en/4.2/howto/deployment/asgi/) for more details.
- **wsgi.py**: An entry-point for WSGI-compatible web servers to serve your project. See [How to deploy with WSGI](https://docs.djangoproject.com/en/4.2/howto/deployment/wsgi/) for more details.

## The development server

To verify your Django project works, change into the outer `mysite` directory and run the following commands

``` sh
py manage.py runserver
```

> [!note] 
> Ignore the warning about unapplied database migrations for now; we’ll deal with the database shortly

Django development server is a lightweight web server written purely in Python for develop things rapidly, without having to deal with configuring a production server – such as Apache – until you’re ready for production.

> [!caution] 
> **Don’t** use this server in anything resembling a production environment. It’s intended only for use while developing. (We’re in the business of making web frameworks, not web servers.)

### Automatic reloading of runserver

The [development server](https://docs.djangoproject.com/en/4.2/ref/django-admin/#django-admin-runserver) automatically reloads Python code for each request as needed. You don’t need to restart the server for code changes to take effect. However, some actions like adding files don’t trigger a restart, so you’ll have to restart the server in these cases

Quit the server with **`Ctrl + C`** or **`Ctrl + Break`**

### Changing the port

By default, the [`runserver`](https://docs.djangoproject.com/en/4.2/ref/django-admin/#django-admin-runserver) command starts the development server on the internal IP at port 8000
If you want to change the server’s port, pass it as a command-line argument. For instance, this command starts the server on port 8080

``` sh
py manage.py runserver 8080
```

If you want to change the server’s IP, pass it along with the port

``` sh
py manage.py runserver 0.0.0.0:8000
```

