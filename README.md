# blogiv#!/usr/bin/env python
"""Django's command-line utility for administrative tasks."""
import os
import sys


def main():
    """Run administrative tasks."""
    os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'blogiv.settings')
    try:
        from django.core.management import execute_from_command_line
    except ImportError as exc:
        raise ImportError(
            "Couldn't import Django. Are you sure it's installed and "
            "available on your PYTHONPATH environment variable? Did you "
            "forget to activate a virtual environment?"
        ) from exc
    execute_from_command_line(sys.argv)


if __name__ == '__main__':
    main()

web: gunicorn blogiv.wsgi --log-file -
"# blogiv" 

asgiref==3.3.4
boto3==1.18.9
botocore==1.21.9
certifi==2020.12.5
chardet==4.0.0
Django==3.2.2
django-filter==2.4.0
django-storages==1.11.1
gunicorn==20.1.0
heroku==0.1.4
idna==2.10
jmespath==0.10.0
Pillow==8.3.1
python-dateutil==2.8.2
pytz==2021.1
requests==2.25.1
s3transfer==0.5.0
six==1.16.0
sqlparse==0.4.1
urllib3==1.26.4
whitenoise==5.3.0

python=3.8.1
