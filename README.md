# django-venv
testing/learning

ubuntu 14.04 python3.4.3 python3.4-venv

Creation:

python3 -m venv django-venv

Session:

source bin/activate

deactivate

Preparation in the session:

pip install --upgrade pip

pip install django

or pip install django~=1.10.4 for version matching


Postgresql backend, basic django site:

pip install psycopg2
django-admin startproject dlog

Not in venv:

su psql

psql

CREATE USER dlog;

CREATE DATABASE dlog_db OWNER dlog;

ALTER USER dlog WITH ENCRYPTED PASSWORD 'bbb';

\q

Make sure to check settings.py in site dir.
Password as bash environment var DBPASS.

In venv:

Populate db:
python manage.py migrate

Start server:
python manage.py runserver

Start app (dlog/settings.py to use it):
python manage.py startapp blog

Add model (class) Post in blog/models.py and make django aware of it:
python manage.py makemigrations blog
Import Post to admin by editing blog/admin.py

Create superuser:
python manage.py createsuperuser
