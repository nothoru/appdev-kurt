# Django installation
* before starting python must be installed 

To install the django type:
```
$ pip install django
``` 
To create a virtual environment:
```
python -m venv "[folder_name]" 
```
installing venv means you are using a virtual environment and to activate use `folder_name\Scripts\activate`.
you can also just install locally.

To create a django project which will generate basic structure and files use:
```
django-admin startproject "[folder_name]"
```
here is the result:
```
folder_name/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
```
Next CD to the created project and install an application by typing:
```
python manage.py startapp ["folder_name"]
```
Go to the settings.py under the project folder and place the newly created application under the INSTALLED_APPS

Create a `urls.py` under the application folder for the urlpatterns which will be associated with views

make sure that at the top of views.py `from django.urls import path`, `from . import views` is written

in project folder urls.py inside the urlpattern make sure to create a path for the application's urls.py 

`path("", include("applcation.urls"))` this is where routing to the application's url's will be handled

 You can now create a function in views.py to render some of the html files and you can also create templates
