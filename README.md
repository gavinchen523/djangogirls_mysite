
# https://tutorial.djangogirls.org
# djangogirls_mysite
# initial enviroment
python -m venv myvenv 
pip install --upgrade pip
pip install django

# Your first Django project!
django-admin startproject mysite . 
  -> modify mysite/settings
   	ALLOW_HOST
	TIME_ZONE
  -> add mysite/settings
  	STATIC_ROOT
python manage.py migrate
python manage.py runserver 0:8000

# Creating an application
python manage.py startapp blog
  -> modify mysite/settings
	INSTALLED_APP
  -> modify blog/models.py
python manage.py makemigrations blog
python manage.py migrate blog

# Django admin
  -> modify blog/admin.py
python manage.py createsuperuser
open "http://127.0.0.1:8000/admin"

# Django urls
  -> modify mysite/urls.py
  -> add blog/urls.py
  -> modify blog/views.py
  -> mkdir -p blog/templates/blog
  -> add blog/templates/blog/post_list.html
open "http://127.0.0.1:8000/" 
  -> show "blog/templates/blog/post_list.html"

# Dynamic data in templates
  -> modify blog/views.py
  -> modify blog/templates/blog/post_list.html

# CSS - make it pretty!
  -> mkdir -p blog/static/css
  -> add blog/static/css/blog.css
  -> modify blog/templates/blog/post_list.html

# CSS - class
  -> modify blog/static/css/blog.css
  -> modify blog/templates/blog/post_list.html

# Template extending
  -> add blog/templates/blog/base.html
  -> modify blog/templates/blog/post_list.html

# Extend your application
#pk -> primaru key
  -> modify blog/urls.py
  -> modify blog/views.py
  -> add blog/templates/blog/post_detail.html

# Django Forms
  -> add blog/forms.py
  -> modify blog/templates/blog/base.html
  -> modify blog/urls.py
  -> modify blog/views.py
  -> add blog/templates/blog/post_edit.html
  -> add blog/templaes/blog/post_detail.htlm
