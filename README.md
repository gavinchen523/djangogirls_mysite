
# https://tutorial.djangogirls.org
# djangogirls_mysite
# initial enviroment
python -m venv myvenv 
pip install --upgrade pip
pip install django

# Your first Django project!
django-admin startproject mysite . 
  -> change mysite/settings
   	ALLOW_HOST
	TIME_ZONE
  -> add mysite/settings
  	STATIC_ROOT
python manage.py migrate
python manage.py runserver 0:8000

# Creating an application
python manage.py startapp blog
  -> change mysite/settings
	INSTALLED_APP
  -> change blog/models.py
python manage.py makemigrations blog
python manage.py migrate blog

# Django admin
  -> change blog/admin.py
python manage.py createsuperuser
open "http://127.0.0.1:8000/admin"

# Django urls
  -> change mysite/urls.py
  -> add blog/urls.py
  -> change blog/views.py
  -> mkdir -p blog/templates/blog
  -> add blog/templates/blog/post_list.html
open "http://127.0.0.1:8000/" 
  -> show "blog/templates/blog/post_list.html"

# Dynamic data in templates
  -> change blog/views.py
  -> change blog/templates/blog/post_list.html

#CSS - make it pretty!
  -> mkdir -p blog/static/css
  -> add blog/static/css/blog.css
  -> change blog/templates/blog/post_list.html




