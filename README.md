# Ex02 Django ORM Web Application
## Date:24/05/25 

## AIM
To develop a Django application to store and retrieve data from a Movies Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM
![image](https://github.com/user-attachments/assets/74e6c40d-788f-47c1-a3d6-d82164fbc3cd)


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
models.py
from django.db import models
from django.contrib import admin
class Movie(models.Model):
	Name=models.CharField(max_length=20,primary_key=True)
	Genre=models.CharField(max_length=20)
	Cost=models.IntegerField()
	Run=models.FloatField()
	Rating=models.IntegerField()
class MovieAdmin(admin.ModelAdmin):
	list_display=("Name","Genre","Cost","Run","Rating")

admin.py
from django.contrib import admin
from .models import Movie,MovieAdmin
admin.site.register(Movie,MovieAdmin)



## OUTPUT
![image](https://github.com/user-attachments/assets/cfb8d58b-e50f-4192-9d76-60cc4d3ebd58)

## RESULT:
Thus the program for creating movies database using ORM hass been executed successfully.


