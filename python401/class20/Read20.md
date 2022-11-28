# Using models
  - Django web applications access and manage data through Python objects referred to as models. Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc. The definition of the model is independent of the underlying database — you can choose one of several as part of your project settings. Once you've chosen what database you want to use, you don't need to talk to it directly at all — you just write your model structure and other code, and Django handles all the dirty work of communicating with the database for you.


## Model primer
### Model definition
  - Models are usually defined in an application's models.py file. They are implemented as subclasses of django.db.models.Model, and can include fields, methods and metadata.
  
        ```

             from django.db import models
              from django.urls import reverse

              class MyModelName(models.Model):
                  """A typical class defining a model, derived from the Model class."""

            # Fields
            my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
            # …

            # Metadata
            class Meta:
                ordering = ['-my_field_name']

            # Methods
            def get_absolute_url(self):
                """Returns the URL to access a particular instance of MyModelName."""
                return reverse('model-detail-view', args=[str(self.id)])

            def __str__(self):
                """String for representing the MyModelName object (in Admin site etc.)."""
                return self.my_field_name

        ```
   
  ### Fields
   - A model can have an arbitrary number of fields, of any type — each one represents a column of data that we want to store in one of our database tables
   
   
 
 ### COMMON FIELD ARGUMENTS
  - help_text : Provides a text label for HTML forms (e.g. in the admin site)
  - verbose_name : A human-readable name for the field used in field labels If not specified, Django will infer the default verbose name from the field name.
  - default : he default value for the field. This can be a value or a callable object, in which case the object will be called every time a new record is created.
  - null : If True, Django will store blank values as NULL in the database for fields where this is appropriate (a CharField will instead store an empty string). The default is False
  - blank : If True, the field is allowed to be blank in your forms. The default is False, which means that Django's form validation will force you to enter a value. This is often used with null=True, because if you're going to allow blank values, you also want the database to be able to represent them appropriately
  - choices :  A group of choices for this field. If this is provided, the default corresponding form widget will be a select box with these choices instead of the standard text field.
  - primary_key :primary_key: If True, sets the current field as the primary key for the model (A primary key is a special database column designated to uniquely identify all the different table records). If no field is specified as the primary key, Django will automatically add a field for this purpose

# Django admin site 
  - The Django admin application can use your models to automatically build a site area that you can use to create, view, update, and delete records. This can save you a lot of time during development, making it very easy to test your models and get a feel for whether you have the right data. The admin application can also be useful for managing data in production, depending on the type of website.
  
  
 ## Registering models
  -  looks like this — note that it already imports django.contrib.admin:
  - ``` from django.contrib import admin ```
  - This code imports the models and then calls admin.site.register to register each of them.
    
    ``` 
       from .models import Author, Genre, Book, BookInstance

      admin.site.register(Book)
      admin.site.register(Author)
      admin.site.register(Genre)
      admin.site.register(BookInstance)   

    ```
 
 ## Creating a superuser
  - ```python3 manage.py createsuperuser```
  - 
        
        




    
