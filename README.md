# Django-practicas
# Para crea proyecto:
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


# Pare hacer un pagina sencilla
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
# Para crear los regisros en el admin

1. migrar y crear el super usuario
   - python manage.py createsuperuser

En la app:
1. models.py
crear la clase que va a contener los espacion que quieres en el admin
-id=models.CharField(primary_key=True,max_length=6)


2. admin.py
mover los modelos a admin
- from django.contrib import admin
- from .models import sucursales

- admin.site.register(sucursales)

3. python manage.py makemigrations
4. python manage.py migrate 

# Para que el registro se vea en la pigina
1. crear una vista en views.py el la lista
   - ejemplo:
   - ![image](https://github.com/user-attachments/assets/29827e38-f115-4a04-9bb6-a61506ef9144)

2. configurar el urls.py
   -  path("",views.listadoAviones,name="listadoAviones")
  
3. crear un plantilla en html
   <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Examen</title>
</head>
<body>

    <h1>sucursales</h1>
    <ul>
        {% for s in misucursal %}
        <li> {{s.id}}  {{s.nombre}}</li>
        {% endfor %}
    </ul>


</body>
</html>


   
   


