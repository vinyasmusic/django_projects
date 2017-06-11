# django_projects
How to start a Django Project ? 

Here is a smart way to do it using the Cookiecutter template :

If you do not intend to use Docker, making a virtualenv is highly recommended.

Create a virtual environment:

` pip install virtualenv `
` virtualenv project_env `
` source /path_to_project_env_/bin/activate `

Install cookiecutter

` pip install cookiecutter `

Now run

` cookiecutter https://github.com/pydanny/cookiecutter-django `

After this you will see options
Enter the values according to your project requirements

```
    project_name [Project Name]: VndlyClone
    project_slug [reddit_clone]: vndly
    author_name [Daniel Roy Greenfeld]: Reckonsys
    email [you@example.com]: pydanny@gmail.com
    description [A short description of the project.]: A vndly clone.
    domain_name [example.com]: myreddit.com
    version [0.1.0]: 0.0.1
    timezone [UTC]: Asia/Kolkata
    use_whitenoise [y]: n
    use_celery [n]: y
    use_mailhog [n]: n
    use_sentry_for_error_reporting [y]: y
    use_opbeat [n]: n
    use_pycharm [n]: y
    windows [n]: n
    use_docker [y]: y
    use_heroku [n]: n
    use_compressor [n]: n
    Select postgresql_version:
    1 - 9.5
    2 - 9.4
    3 - 9.3
    4 - 9.2
    Choose from 1, 2, 3, 4 [1]: 1
    Select js_task_runner:
    1 - Gulp
    2 - Grunt
    3 - None
    Choose from 1, 2, 3, 4 [1]: 3
    use_lets_encrypt [n]: n
    Select open_source_license:
    1 - MIT
    2 - BSD
    3 - GPLv3
    4 - Apache Software License 2.0
    5 - Not open source
    Choose from 1, 2, 3, 4, 5 [1]: 1
    use_elasticbeanstalk_experimental: n 
```

If using docker : 

Add the docker-machine ip to settings ALLOWED_HOSTS field 

Go to project folder
` cd /project_folder/ `

Build the project for development
` docker-compose -f dev.yml build `

Run the dev system 
` docker-compose -f dev.yml up `

Cookiecutter Documentation : http://cookiecutter-django.readthedocs.io/en/latest/index.html

Other cookiecutter projects can be found at : https://github.com/audreyr/cookiecutter

Whitenoise : http://whitenoise.evans.io/en/stable/

Mailhog : https://github.com/mailhog/MailHog

Sentry : https://docs.sentry.io/clients/python/

Opbeat : https://opbeat.com/django

Compressor : https://django-compressor.readthedocs.io/en/latest/

Let's Encrypt : https://github.com/urda/django-letsencrypt

