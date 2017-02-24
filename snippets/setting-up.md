## Getting started

### Setting up

#### Virtualenv

```
virtualenv -p python3.4 env3.4
```

* `-p` allows you to specify a python executable
* `env3.4` can be a path to anywhere on you filesystem

**to activate your virtualenv**

```
source env3.4/bin/activate
```

Now anything you install will be installed within this virtualenv and not systemwide

#### Requirements

**requirements.txt**

```
django==1.10
djangorestframework==3.5
```

* make sure to specify versions

**requirements-dev.txt**

> Utilities to make dev better

```
ipython
ipdb
mock
responses
sniffer

pylint
coverage
django_nose
pinocchio
nose-html-reporting
Faker
```

#### Start your project

```
django-admin.py startproject expenseservice
```

```
python manage.py startapp {appname}
```

#### Project layout:

```
```

#### App layout:

This is what a rather complete app might look like:

```
.myapp
  |_ api.py
  |_ serializers.py
  |_ models.py
  |_ managers.py
  |_ permissions.py
  |_ filters.py
  |_ signals.py
  |_ validators.py
  |_ tests/
     |_ __init__.py
     |_ test_models.py
     |_ test_serializers.py
     |_ ...

```

#### Settings.py

**AUTH_USER_MODEL**
```
AUTH_USER_MODEL = 'auth.User'
```


