# COLINHA
Uma pequena cola pessoal

# Criar projeto Django usando pipenv
```
pip install --upgrade pip
pip install pipenv
pip install --upgrade pipenv
pip install python-decouple
pipenv --three
pipenv install django
pipenv install python-decouple
pipenv install dj-database-url
pipenv install dj-static
pipenv install django-extensions
pipenv install django-test-without-migrations
pipenv install django-debug-toolbar
pipenv shell
django-admin startproject project .
mkdir apps
python manage.py startapp core
MOVA OS APPS CRIADOS PARA DENTRO DA PASTA "apps"
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
```
CRIE UM ARQUIVO ".env" E INSIRA OS DADOS:
```
DEBUG=True
SECRET_KEY=INSIRAASECREKEY
```
INSIRA EM "settings.py":
```
from decouple import config
```
ALTERE EM "settings.py":
```
SECRET_KEY = config('SECRET_KEY')
DEBUG = config('DEBUG', default=False, cast=bool)
```
INSIRA EM "settings.py" > "INSTALLED_APPS":
```
'apps.core',
```
PARA EXECUTAR O SERVIDOR:
```
python manage.py runserver
```
