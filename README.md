# appdev-kurt
* before starting python must be installed
1. pip install django 
2. python -m venv "[folder_name]" Ex. .venv
- installing venv means you are using a virtual environment and to activate use .folder_name\Scripts\Activate
- you can also just install locally
3. django-admin startproject "[folder_name]" Ex. demo
- your installing the django framework
4. Next CD to the created folder and install an application by typing [python manage.py startapp ["folder_name"] Ex. myapp]
5. Go to the settings.py under the root folder and place the newly created application under the INSTALLED_APPS
6. Create a urls.py under myapp for the urlpatterns which will be associated with views
- make sure that at the top "from django.urls import path", "from . import views" is written
7. in root folder urls.py inside the urlpattern make sure to create a path for the application's urls.py 
- path("", include("applcation.urls")) this is where routing to the application's url's will be handled
8. At this point you can just create a function in views.py to render some of the html files and you can also create templates