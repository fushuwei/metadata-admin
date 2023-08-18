# metadata-admin

## Project description

Metadata admin is a metadata management system developed using the django rest framework.

### Features

Supports multiple data sources, as follows:

- MySQL
- Oracle
- SqlServer
- PostgreSQL
- ClickHouse

### Requirements

- Python >= 3.10.11
- Django >= 4.2.4
- MySQL  >= 8.0

## Get started

### Installation

- Download

```shell
git clone git@github.com:fushuwei/metadata-admin.git
```

- Install virtual environment

```shell
# Creating a virtual environment
python -m venv venv

# Activate virtual environment (On Windows use `venv\Scripts\activate`)
source venv/bin/activate

# Exit virtual environment
deactivate
```

- Install dependencies

```shell
# Install pipreqs
pip install pipreqs

# Generate requirements.txt, "." is current directory
pipreqs . --encoding=utf8 --force

# Install project dependency
pip install -r requirements.txt
```

### Configuration

- Database

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'HOST': 'localhost',
        'USER': 'postgres',
        'PASSWORD': '123456',
        'NAME': 'postgres',
    },
    'clickhouse': {
        'ENGINE': 'clickhouse_backend.backend',
        'NAME': 'default',
        'HOST': 'localhost',
        'USER': 'DB_USER',
        'PASSWORD': 'DB_PASSWORD',
    }
}
```

### Quickstart

```shell
python manage.py runserver --settings config.settings.develop
```

### Project Structure

omit

## References

- Official documents (required reading)
    - `https://docs.djangoproject.com/zh-hans/4.2`
    - `https://www.django-rest-framework.org`


- Open source projects
    - `https://github.com/Mischback/django-project-skeleton`
    - `https://github.com/saqibur/django-project-structure`
    - `https://github.com/rdegges/django-skel`
    - `https://gitee.com/zhengxiangqi/template-for-django`
    - `https://github.com/fushuwei/django-base-demo`

## You maybe interested

- How to create a django projects from scratch

```shell
# Create the project directory
mkdir project_name
cd project_name

# Create a virtual environment to isolate our package dependencies locally
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# Install Django and Django REST framework into the virtual environment
pip install django
pip install djangorestframework

# Set up a new project with a single application
django-admin startproject config .

# Create app
mkdir apps
cd apps
django-admin startapp app_name

...
```
