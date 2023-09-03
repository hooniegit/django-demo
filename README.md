# django-demo

# installation
``` bash
$ pip install django==1.8
```

# start project
``` bash
$ django-admin startproject demo .
```
``` python
django-demo
├───manage.py # site management
└───demo
        settings.py # web page settings
        urls.py # pattern list for urlsolver
        wsgi.py
        __init__.py
```

# settings.py
``` python
# change timezone to seoul
TIME_ZONE = 'Asia/Seoul'
```
``` python
# add static files' path
STATIC_ROOT = os.path.join(BASE_DIR, 'static')
```

# migrate (create database)
``` bash
$ python3 manage.py migrate

Operations to perform:
  Apply all migrations: admin, auth, contenttypes, sessions
Running migrations:
  Applying contenttypes.0001_initial... OK
  Applying auth.0001_initial... OK
  Applying admin.0001_initial... OK
  Applying admin.0002_logentry_remove_auto_add... OK
  Applying contenttypes.0002_remove_content_type_name... OK
  Applying auth.0002_alter_permission_name_max_length... OK
  Applying auth.0003_alter_user_email_max_length... OK
  Applying auth.0004_alter_user_username_opts... OK
  Applying auth.0005_alter_user_last_login_null... OK
  Applying auth.0006_require_contenttypes_0002... OK
  Applying auth.0007_alter_validators_add_error_messages... OK
  Applying auth.0008_alter_user_username_max_length... OK
  Applying auth.0009_alter_user_last_name_max_length... OK
  Applying sessions.0001_initial... OK
```

# run webserver
``` bash
$ python3 manage.py runserver

Performing system checks...

System check identified no issues (0 silenced).
September 03, 2023 - 14:37:37
Django version 2.0.13, using settings 'demo.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```