# Django REST Framework & Docker



## Django REST Framework 
  - Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework. It always must be added to a project after Django itself has been installed and configured.


##  Docker
  - With Docker it doesn’t matter if you are using a Mac, Windows, or Linux computer anymore. The entire development environment is isolated: programming language, software packages, databases, and more.
  - With Docker we now longer have to mess around with virtual environments. We can faithfully reproduce a production environment locally. 
  - Docker can be shared among team members so everyone is working on the same setup.

## Containers vs Virtual Environments
  - Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.
  - But…virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper version. So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment.

## Install Docker
  - e can confirm the correct version is running. It should be at least version 19.
  -   ``` 
       docker --version
        Docker version 19.03.5, build 633a0
      ```

## Images and Containers
 ### A baking analogy we can use here is as follows:
   - A Dockerfile is the recipe for a cake
   - An image is a snapshot of the recipe at a given time
   - A docker-compose.yml says how to make the cake
   - And the container is the actual, baked cake
 
 ## Conclusion
  - Docker is a way to run Linux containers
  - Containers are a lightweight alternative to Virtual Machines
  - Dockerfile is a list of instructions for creating an image
  - Images are made up of one or more layers
  - Containers are a running instance of an image
  - docker-compose.yml controls how to run the container
  
    
