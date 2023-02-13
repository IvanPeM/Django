# Django

## Como instalar Django en Ubuntu
***
1. Actualizar Python
```
$ sudo apt-get install upgrade
```
2. Instalar Pip
Se tiene que instalar el comando pip en https://bootstrap.pypa.io/get-pip.py.
Y se tiene que ir a la carpeta donde se ha instalado.
```
$ python3 get-pip.py
```
3. Instalar Django
```
$ python3 -m pip install Django
```
4. Comprobar si funciona Django
```
$ python3 -m django --version
$ python3
>>> import django
>>> print(django.get_version())
```
5. Instalar django-admin
```
$ sudo apt install python3-django
```
6. Creando un proyecto
```
$ django-admin startproject mysite
```
7. Encender el proyecto
```
$ cd mysite
$ python3 manage.py runserver
```
8. Entra en el navegador
```
127.0.0.1:8000
```
9. Poder crear la aplicación
```
$ python3 manage.py startapp polls
```
10. Cambiar views.py
```
$ cd polls
$ nano views.py
```
Y escribimos lo siguiente
```
from django.http import HttpResponse

def index(request):
	return HttpResponse("Hello, world.")

```
11. Crear urls.py
```
$ touch urls.py
```
12. Escribir dentro de urls.py
```
from django.urls import path

from . import views

urlpatterns = [
    path('', views.index, name='index'),
]
```

