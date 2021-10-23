# gala_coding_club_initial_project

## Django Project Start Instructions


## Starting a project. 

I like create a "super folder" for a project. This will be the 
git repo, and will contain files not directly in the project, 
including the virtual environemnt, a local notes file that 
I don't push to the repo as well as Docker compose Yaml file,
if needed.

## make super folder:
### SKIP THIS IS YOU ALREADY HAVE PROJECT FOLDER
```bash
mkdir our_app
cd our_app
```
## make virtual environemnt. 

command line switch -m to allow modules to be located using the Python module namespace for execution as scripts.
```bash
python3 -m venv venv
source venv/bin/activate
```
## make a requrements.txt file. 

```bash
echo "Django>=3.2.6,<3.3" > requirements.txt
python -m pip install --upgrade pip
pip install -r requirements.txt
```
## change to the project directory
```bash
cd our_app
python -m django startproject app . # Prefered mthod - with the period places prject in current folder

python -m django startproject app myapp # places it in a new myapp directory
python -m django startproject app # creates a directory call app
or django-admin startproject ... instead of python -m django startproject
```
## run dev server
```bash
python app/manage.py runserver
```
## OR only if you need to specify the address.
```bash
python app/manage.py runserver localhost:8000 
```

### When using replit.com do the following:

- In the main folder our_app add a file called `.replit` which can be done from the bash shell:
```bash
touch .replit
```
- Add the following to the `.replit` file:

```bash
language = "python3"
run = "python app/manage.py runserver 0.0.0.0:8000"
```


## add views inside the app folder:
```
mkdir app/views.py
```
