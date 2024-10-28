# Django-practicas
crea proyecto:
1. crear una carpeta en el disco duro,y una dentro de esta
2. abrir la carpeta
3. abrir el terminal
4.  py -3 -m venv .venv
5.  python -m pip install --upgrade pip
6.  python -m pip install django
7.  .venv\scripts\activate.bat  //con el nombre de el entorno visual
8.  seleccionar el entorno visual
9.  django-admin startproject proyecto_vet .
10.   python manage.py startapp app_veterinaria
11.   python manage.py runserver
12.   crar la carpeta templates con los archivos html



En el proyecto:

settings.py 
1. añadir la app en linea 33
2. creae la base de datos: NAME: 'veterinaria.db' linea 80
3. cambiar idioma 'es.mx' linea 107


En la app:
1. crear un archivo urls.py:
- from django.urls import path
- from  appveterinaria import views
- urlpatterns = [
-       path("",views.tablasucursal,name="tablasucursal"),
         ]

2. en el archivo views el siguiente codigo:
- from django.urls import path
- from  appveterinaria import views
- urlpatterns = [
-     path("",views.tablasucursal,name="tablasucursal"),
]

En el proyecto:
urls.py
1.  agrego ,include
2.  agreagar el urls de la app  
- path("",include("appveterinaria.urls"))
- 

   


