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

django-admin startproject dlog

su psql

psql

CREATE USER dlog;

CREATE DATABASE dlog_db OWNER dlog;

ALTER USER dlog WITH ENCRYPTED PASSWORD 'bbb';

\q

Check settings.py in site dir.
Password as bash environment var DBPASS.


Populate db:
python manage.py migrate

Start server:
python manage.py runserver
