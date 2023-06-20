# Python commands

## This is to create virtual env

```python
> python3 -m venv env

> source env/bin/activate

> deactivate (to come out of that env)

> pip3 freeze (To check all the installed dependencies)

> cmd+shift+p create virtual env and open bash to have venv specific to project

> pip3 install django and check pip3 freeze
```

# Django Refresher

## Inside .venv i.e bash

## cd into the foodOnline folder

## To create boiler plate django code

```python
> django-admin startproject projectname .

> e.g django-admin startproject foodOnline_main .
```

## To run the django code

```python
> python3 manage.py runserver
```

## To access the admin console

```python
> localhost:8080/admin

> For username and password run below command
> python manage.py migrate
> python3 manage.py createsuperuser

username: djangoadmin
email: djangoadmin@gmail.com
pass: Asgi!123
```

## To link it to templates folder.

1. Create a templates folder and add html files.
2. In setting.py inside TEMPLATES --> DIRS --> 'templates' folder name which is created
3. Update the urls.py to add home url which links to a method in view
4. Inside this view create a method named in urls.py and add a render function pointing to home.html inside templates folder

## Static File Linking

1. create a static folder inside project folder
2. Inside setting.py add below lines
   ```python
    STATIC_ROOT = BASE_DIR /'static'
    STATICFILES_DIRS =[
        'foodOnline_main/static'
    ]
   ```
3. Inside home.html in the start of line add this **{% load static %}**
4. Then for every static file load static using templating
   ```htm
   <!-- CSS -->
   <link href="{% static 'css/iconmoon.css' %}" rel="stylesheet" />
   <link href="{% static 'css/style.css' %}" rel="stylesheet" />
   <link href="{% static 'css/cs-foodbakery-plugin.css' %}" rel="stylesheet" />
   <link
     rel="stylesheet"
     href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css"
   />
   <link href="{% static 'css/bootstrap-slider.css' %}" rel="stylesheet" />
   ```
5. python manage.py collectstatic (to collect static files outside of folder this is used in production didnt understand properly)

## To create django app

```python
> python3 manage.py startapp employees

```

## After creating the model objects and adding it into setting.py run the below command to migrate models to tables

```python
> python3 manage.py makemigrations (This will create a sql file in migrations folder)

> python3 manage.py migrate (This will actually create database)
```

# DjangoPriyasRestaurant

![Alt text](assets/FoodOnline-Flowchart.png)
