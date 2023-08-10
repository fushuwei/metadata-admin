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
# Creating virtual environment
python -m venv venv

# Activate the virtual environment (Scripts directory on Windows, bin directory on Linux)
venv\Scripts\activate

# Exit virtual environment
# deactivate
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

### Run Server

```shell
python manage.py runserver --settings config.settings.develop
```

### Project Structure

`todo`

## References

- `https://github.com/rdegges/django-skel`
- `https://github.com/Mischback/django-project-skeleton`
- `https://github.com/saqibur/django-project-structure`
- `https://github.com/fushuwei/django-base-demo`
- `https://gitee.com/zhengxiangqi/template-for-django`

## You maybe interested

- How to create django projects from scratch

```shell
# The project_name directory must be created in advance
django-admin startproject config project_name
```
