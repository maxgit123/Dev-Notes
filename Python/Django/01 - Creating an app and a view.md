## Creating an app

Each application you write in Django consists of a Python package that follows a certain convention. Django comes with a utility that automatically generates the basic directory structure of an app, so you can focus on writing code rather than creating directories.

> [!note] Projects vs. apps
> What’s the difference between a project and an app? An app is a web application that does something – e.g., a blog system, a database of public records or a small poll app. A project is a collection of configuration and apps for a particular website. A project can contain multiple apps. An app can be in multiple projects. 

Your apps can live anywhere on your [Python path](https://docs.python.org/3/tutorial/modules.html#tut-searchpath "(in Python v3.11)"). We’ll create our app in the same directory as your `manage.py` file so that it can be imported as its own top-level module, rather than a submodule of `mysite`.

To create your app, make sure you’re in the same directory as `manage.py` and the server is stopped (`Ctrl + C`), then type this command:

``` sh
py manage.py startapp <myapp>
```

## Creating a view

Open the file `myapp/views.py` and put the following Python code in it:

``` Python
from django.http import HttpResponse

def index(request):
    return HttpResponse("Hello, world. You\'re at the myapp index.")
```

To call the view, we need to map it to a URL in a URLconf.
To create a URLconf in the `myapp` directory, create a file called `urls.py`. 
In the `<myapp>/urls.py` file include the following code:

``` Python
from django.urls import path
from . import views

urlpatterns = [
    path("", views.index, name="index"),
]
```

The next step is to point the root URLconf at the `<myapp>.urls` module.
In `<mysite>/urls.py`, add an import for `django.urls.include` and insert an [`include()`](https://docs.djangoproject.com/en/4.2/ref/urls/#django.urls.include "django.urls.include") in the `urlpatterns` list, so you have:

``` Python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
	path("admin/", admin.site.urls),
    path("myapp/", include("myapp.urls")),
]
```

> [!note] When to use `include()`
> You should always use `include()` when you include other URL patterns. `admin.site.urls` is the only exception to this.

You have now wired an `index` view into the URLconf. Verify it’s working with the following command:

``` sh
py manage.py runserver
```
