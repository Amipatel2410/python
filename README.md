# python

step1: Install python latest version 3.6.2
  via https://www.python.org/downloads/
  
step2: In Terminal Command:
   $ python
   Python 3.4.x
   [GCC 4.x] on linux
   Type "help", "copyright", "credits" or "license" for more information.
   >>>
   
 # Introduction to Django
 
  Django is a high-level Python framework that enables rapid development of secure and maintainable websites
  Django is free and open source framework Django take security features and helps developers avoid many common security mistakes
  Excellent lightweight server for development and testing. It is Good templating language.
  
 => Django Installation
  step:1 Install Git
  
  step2: Check out Django’s main development branch
		$ git clone git://github.com/django/django.git 
    
  step3: Create virtualenv on Python 3
  step:4 Create folder  
    $ mkdir ~/.virtualenvs
    
  step:4 Create a new virtualenv by running:
    $ python3 -m venv ~/.virtualenvs/djangodev
    
  step:4 Install pip 
    $ pip3 install virtualenv
    
  step:5 To activate virtualenv
    $ source ~/.virtualenvs/djangodev/bin/activate
    
    => Verifying if Django installed successfully or not(it gives version of that Django)
    >>> import django
    >>> print(django.get_version())
    1.11
    
    Creating a Project
    
    step1: From the command line, cd into a directory where you’d like to store your code, then run the following command:
      $ django-admin startproject mysite 
      (This will create a mysite directory in your current directory)
      
    step2: Run Development Server
      $ python manage.py runserver
      
    step3: Creating polls app
      $ python manage.py startapp polls
     
    step4: That’ll create a directory polls, which is laid out like this:
      polls/
          __init__.py
          admin.py
          apps.py
          migrations/
              __init__.py
          models.py
          tests.py
          views.py
          
      step5:  In polls/views.py file: This is the simplest view possible in Django. 
              To call the view, we need to map it to a URL - and for this we need a URLconf.
      
      from django.http import HttpResponse
      def index(request):
            return HttpResponse("Hello, world. You're at the polls index.")
            
      step6: In polls/urls.py
                                        
      from django.conf.urls import url

          from . import views

          urlpatterns = [
              url(r'^$', views.index, name='index'),
          ]


