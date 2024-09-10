# Welcome To Damitwhy's Django-Template
I've been pretty frustrated when switching between Linux and Windows versions of VS Code then having issues with permissions so I've set up my Venv on the Linux Debian system first and created this template for future setups, just saving alittle time and having all the installed dependencies in place from the start... Totally clean urls.py files, though there are a few place holder core/template/core files.
Will be adding to this template over time with Django-allauth account template files, static and staticfiles folders.
## Requirements.txt
asgiref==3.8.1
bleach==6.1.0
blinker==1.8.2
certifi==2024.8.30
charset-normalizer==3.3.2
click==8.1.7
cloudinary==1.41.0
dj-database-url==2.2.0
Django==5.0.7
django-allauth==64.0.0
django-appconf==1.0.6
django-cloudinary-storage==0.3.0
django-imagekit==5.0.0
django-summernote==0.8.20.0
Flask==3.0.3
gunicorn==22.0.0
idna==3.8
itsdangerous==2.2.0
Jinja2==3.1.4
MarkupSafe==2.1.5
packaging==24.1
pilkit==3.0
pillow==10.4.0
psycopg2==2.9.9
psycopg2-binary==2.9.9
python-decouple==3.8
python-dotenv==1.0.1
requests==2.32.3
six==1.16.0
sqlparse==0.5.1
typing_extensions==4.12.2
urllib3==2.2.2
webencodings==0.5.1
Werkzeug==3.0.3
whitenoise==6.7.0
## .gitignore
core.Microsoft*
core.mongo*
core.python*
env.py
__pycache__/
*.py[cod]
node_modules/
.github/
cloudinary_python.txt
db.json
.env
debug.log
wsgi.py
## Installation
Installation instructions.
- Create new repository with this template.
- Open your New repository in VSCode desktop with the GitHub desktop app.
- Create Venv (python) environment if its not already created then activate the Venv folder (python environment) with this command :   < .\venv\Scripts\activate >
- Then install all dependancies from the requirements.txt with command:< pip3 install -r requirements.txt >
- Runserver to see the Django opening page with command:< python3 manage.py runserver >
- Now you have a fairly fresh Django application waiting for you to make use of by wiring up your urls.py and views.py files.
- Remember always to set debug to false in setting.py file before deploying. Sites like Heroku are great for testing your deployments.
- There tends to be a warning that no migrations have been made when you first runserver but this doesnt stop the Django page from loading up, I've normally waited to migrate until i've started to fill the models.py file with the ERD model that I require moving forward.
- When you're ready to migrate use command:< python3 manage.py makemigrations >:this lets you know which migrations will take place then command:< Python3 manage.py migrate >:this writes to the database you've chosen to host your data, Django's default data base is db.sqlite3 which is a file in the root directory but you may be better of with an off site database like PostgreSQL, MySQl or one I've not used like mongodb maybe.
