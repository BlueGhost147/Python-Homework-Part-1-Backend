# Python-Homework-Part-1-Backend

* Subject: SWENGS
* Homework1
* Author: Andreas RAITH
* Topic: Foodproducts

## Requirments
* python 3.8.0 with pip installed
* A Virtual Environment with Django 2.2.7
* A working django project

## Setup
Clone the git repository and copy the app in the project folder
````bash
git clone <RepositoryLink>
````

Add the following line to the urls.py of the project
````python
path('',include('product_manager.urls')),
````

Add the app and the rest_framework to the installed apps in the settings.py of the project
````python
INSTALLED_APPS = [
    (...)
    'product_manager',
    'rest_framework',
]
````

Run the server
````bash
python manage.py runserver
````

### Troubleshooting
If django throws the error 'No such table'
See: https://stackoverflow.com/questions/12784835/django-no-such-table
````bash
python manage.py migrate --run-syncdb
````
