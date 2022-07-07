# Requirements 
- Python3, pip
- PostgreSQL

## Install project and all dependencies
### Python

- Install any python3 version from https://www.python.org/downloads/

Create a new project (virtual environment will be created automatically) in PyCharm and clone Git repository and open repo folder
   

```
git clone <clone address>
cd <name of cloned repository>
```
Install Django and other packages for your Backend
```
pip install -r requirements.txt
```

## Connect PostgreSQL

- Run PostgreSQL Server on your PC (you can download Postgres here https://www.postgresql.org/download/)
- Manualy create a db in Postgres

For managing DB you can use pgAdmin(https://www.pgadmin.org/download/)
- In pgAdmin or any other Postgres GUI connect(or create and then) to your server and create DB
- In settings.py configure your DB with Django(Find DATABASES dict variable and set it like below)

### For mac os
To start the postgres server

```
brew services start postgresql
```

It should look like this
```
.../config/setting.py
    
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.postgresql_psycopg2',
            'NAME': '<your_db_name>',
            'USER': '<your_username>',
            'PASSWORD': '<your_password>',
            'HOST': '<your_host>', # localhost as default
            'PORT': '5432',
        }
    }
``` 

## Run Server

In repositoty root directory run these lines in terminal

For set up:
```
    python3 manage.py makemigrations
    python3 manage.py migrate
``` 
For run server:
``` 
    python3 manage.py runserver
``` 
