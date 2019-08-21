# Python tutorial

### Requirements:

- Install `python 3.6+` via [asdf](https://asdf-vm.com)
- Install [pipenv](https://docs.pipenv.org)

### Start a new project

1\. First, create the `~/workspace` and create a folder for your project.

```sh
mkdir -p ~/workspace/python-tutorial && cd $_
```

2\. Start the project with `pipenv`, that it's good dependencies manager.

```sh
pipenv --python 3.6
pipenv shell
pipenv check
```

3\. Configure [django](https://www.djangoproject.com/) web framework.

Install django dependencies.

```sh
pipenv install django
pipenv install django-extensions --dev
```

Start a django project.

```sh
django-admin startproject pysample .
python manage.py migrate
python manage.py runserver
```

4\. Export dependencies to file `requirements.txt`.

List all dependencies installed in the current environment.

```sh
pipenv run pip freeze
```

Export all dependencies needed to the project.

```sh
pipenv lock -r > requirements.txt
```