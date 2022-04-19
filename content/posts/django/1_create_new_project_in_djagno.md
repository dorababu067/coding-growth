---
title: "Creating new project in django"
date: 2022-04-15T04:40:06+05:30
tags: ["Djagno"]
categories: ["Django"]
---

`Django` is a high-level Python web framework that encourages rapid development and clean, pragmatic design. Django makes it easier to build better web apps more quickly and with less code. It’s free and open source.



django installation

```
pip install django
```
**make sure [django is installed ](https://docs.djangoproject.com/en/4.0/topics/install/) in your mechine before using the below command**

create django project, in place of `starter` you can give your own project name

```
django-admin startproject starter
```
create app in django project, in place of `app1` you can give your own app name

```
cd starter

python manage.py startapp app1
```


once project is created go to you project directory, you will see th below project structure

```

├── app1         #app name
│   ├── admin.py
│   ├── apps.py
│   ├── __init__.py
│   ├── migrations
│   │   └── __init__.py
│   ├── models.py
│   ├── tests.py
│   └── views.py
├── manage.py
└── starter       #project name
    ├── asgi.py
    ├── __init__.py
    ├── __pycache__
    │   ├── __init__.cpython-38.pyc
    │   └── settings.cpython-38.pyc
    ├── settings.py
    ├── urls.py
    └── wsgi.py

4 directories, 15 files

```
for writing first view function go to `views.py` in your app directory

```
# app1/views.py


from django.shortcuts import render
from django.http import HttpResponse

# Create your views here.

def index(request):
    return HttpResponse("<h1>Hello world<h1>")

```
once function is completed we have to write the url in urlpatterns.
go to` urls.py` file in your project directory import what function you have wite in the `views.py
` and wite url for that function like below
```
#starter/urls.py


from django.contrib import admin
from django.urls import path
from app1.views import index  

urlpatterns = [
    path("admin/", admin.site.urls),
    path("/", index, name="index"),
]


```

once `urls.py ` setup completed run the server using hte below command

```
python manage.py runserver
```
server is started without any errors you can able to see the below output

```

Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
April 19, 2022 - 01:05:06
Django version 4.0.4, using settings 'starter.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.

```

go to browser open this [http://127.0.0.1:8000](http://127.0.0.1:8000) url you can see the below output

![image](/images/django/1_hello_world.png)