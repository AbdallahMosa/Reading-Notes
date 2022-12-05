# Django Custom User

## Setup 
  - To start, create a new Django project from the command line. We need to do several things:
    - install Django
    - make a new Django project called django_project
    - make a new app accounts
    - start the local web server

## AbstractUser vs AbstractBaseUser
  - There are two modern ways to create a custom user model in Django: AbstractUser and AbstractBaseUser. In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work

## Custom User Model
  - update django_project/settings.py
  - create a new CustomUser model
  - create new UserCreation and UserChangeForm
  - update the admin

## Superuser
  - `python manage.py createsuperuser`

## DjangoX 
  - Installation
  - 
   ```
    git clone https://github.com/wsvincent/djangox.git
    cd djangox
  ```
  
  - ```

      $ python -m venv .venv

      # Windows
      $ Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
      $ .venv\Scripts\Activate.ps1

      # macOS
      $ source .venv/bin/activate

      (.venv) $ pip install -r requirements.txt
      (.venv) $ python manage.py migrate
      (.venv) $ python manage.py createsuperuser
      (.venv) $ python manage.py runserver
      # Load the site at http://127.0.0.1:8000

