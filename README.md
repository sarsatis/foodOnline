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
## To create django app
```python
> python3 manage.py startapp employees

> python manage.py migrate
```
## To access the admin console
```python
> localhost:8080/admin

> For username and password run below command

> python3 manage.py createsuperuser
```
## After creating the model objects and adding it into setting.py run the below command to migrate models to tables
```python
> python3 manage.py makemigrations (This will create a sql file in migrations folder)

> python3 manage.py migrate (This will actually create database)
```


# DjangoPriyasRestaurant

![Alt text](assets/FoodOnline-Flowchart.png)