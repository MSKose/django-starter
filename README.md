# settings.py configuration

💡 NOTE: this Django repo is opinionated in that it comes with `drf_yasg` (a 3rd party swagger package) and `django-debug-toolbar` already installed and configured. See the notes on those [here](https://github.com/MSKose/django-notes/blob/master/Django%20Fundamentals/django-settings-starter/README.md). Also, sqlite for dev and postgresql for prod settings was chosen. Therefore, after cloning this repository, keep those in mind and change the parts to your linking.



### Installation

```python
# 1. step (creating an environment)
python -m venv env

# 2. step (activating)
source env/bin/activate (for MacOs)
env/Scripts/activate (for Windows)

# this command should return nothing. If it returns something as of now, it could mean you are not running on the new environment
pip freeze

# 3. run the dependencies for this project
pip install -r requirements.txt

# 4. Add the following to your .env file
    SECRET_KEY=<yourSecretKeyHere>
    DEBUG=True 
    ENV_NAME=dev 
    SQL_DATABASE=<yourDatabaseProjectName>
    SQL_USER=<yourDatabaseUsername> 
    SQL_PASSWORD=<yourDatabasePassword>
    SQL_HOST=localhost 
    SQL_PORT=5432

# migrate your initial settings to your database
python manage.py migrate

# running the server
python manage.py runserver
```

- After setting up new dependencies run these commands:

```python
# to see the installed dependencies:
pip freeze

# to save the dependencies (run this command everytime you install a new dependency to make it up-to-date with your dependencies):
pip freeze > requirements.txt
```

- See the [requirements](./requirements.txt) file for the dependency versions