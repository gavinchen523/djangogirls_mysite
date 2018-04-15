
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


