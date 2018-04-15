
# https://tutorial.djangogirls.org
# djangogirls_mysite
# initial enviroment
python -m venv myvenv 
pip install --upgrade pip
pip install django

# Your first Django project!
django-admin startproject mysite . 
  -> change
   	ALLOW_HOST
	TIME_ZONE
  -> add
  	STATIC_ROOT
