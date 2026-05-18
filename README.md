# Ex01 Django ORM Web Application
## Date: 18/05/2026

## AIM
To develop a Django application to manage an online food delivery platform like Zomato/Swiggy using Object Relational Mapping (ORM).

## ENTITY RELATIONSHIP DIAGRAM



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
```
admin.py

from django.contrib import admin
from .models import Car

class CarAdmin(admin.ModelAdmin):
    list_display = ('car_id', 'manufacturer', 'model_name', 'year', 'price')
    list_filter = ('year', 'manufacturer')
    search_fields = ('model_name', 'manufacturer')

admin.site.register(Car, CarAdmin)

models.py

from django.db import models

class Car(models.Model):
    car_id = models.IntegerField()
    model_name = models.CharField(max_length=100)
    manufacturer = models.CharField(max_length=100)
    year = models.IntegerField()
    price = models.FloatField()

    def str(self):
        return f"{self.manufacturer} {self.model_name} ({self.year})"

```



## OUTPUT

<img width="1368" height="868" alt="image" src="https://github.com/user-attachments/assets/4a580721-ecc4-4aa9-ba11-5f703abba1c9" />

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
