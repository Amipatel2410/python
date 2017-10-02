# python

1. Dynamic, interpreted (bytecode-compiled) language
2. No type declarations of variables, parameters, functions, or methods in source code
3. Makes the code short and flexible
4. Python tracks the types of all values at runtime and flags code that does not make sense as it runs.

=> High-level view of PYTHON internals
Lexing : Breaking line of code
Parsing : takes  tokens and generate a structure according to relationship 
Compiling : Turns into one or more code
Interpreting : takes code object and execute code it represent


step1: Install python latest version 3.6.2
  via https://www.python.org/downloads/
  
step2: In Terminal Command:
   $ python
   Python 3.4.x
   [GCC 4.x] on linux
   Type "help", "copyright", "credits" or "license" for more information.
   >>>
   
  => PYTHON Source Code
	- Python is Case-Sensitive
	- Python does not require semicolon at the end of the sentence
	- Comments begins with ’#’ and extend to the end of the line
	- Python source files use “.py” extension and  are called modules
	- To Run Python File:
		>>> python hello.py

=> PYTHON Strings
	- Python has a built-in string class named “str”
	- String literals can be enclosed by either double or single quotes
	- Python strings are “immutable” which means they can not be changed after they are created
	  Characters in string can be accessed using standard [ ] syntax
		For ex.  
		S = ‘hi’
		print s[1]           	##1
		Print len(s)	   	 ##2
		Print  S +  ‘there’   	## hi there
		
=> PYTHON Lists
	List literals are written within square brackets [ ].
		For ex.
		colors = [‘red’ , ‘blue’ , ‘green’]
		print colors[0]  		## red
		print colors[2] 		## green
		print len(colors)		## 3 gives length of list
		
	



 # Introduction to Django
 
  Django is a high-level Python framework that enables rapid development of secure and maintainable websites
  Django is free and open source framework Django take security features and helps developers avoid many common security mistakes
  Excellent lightweight server for development and testing. It is Good templating language.
  
  
 => Django Features:
	- Fully Loaded
	- Reassuringly Secure
	- Exceedingly Scalable
	- Incredibly Versatile
	- Portable

=> Django source File
	- URLs:  URL mapper is used to redirect HTTP requests to the appropriate view based on the request URL. Also 		match patterns of string or digits that appear in an URL
	- View: View is a request handler function, which receives HTTP request and return HTTP Response
	- Models: Models are Python objects that define the structure of an application’s data, and provide mechanisms to 		manage (add, modify, delete) and query records in database.
	- Templates: A template is a text file defining the structure or layout of a file as HTML page with placeholders used 		to represent actual content

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


