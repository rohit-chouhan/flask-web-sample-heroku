# Sample Application for Flask
A sample web and guide to deploy your Flask/Python application to Heroku

### Step 1
- Go to Heroko Website , Login It
- Click on New Application on RIght Top Side
- Give You App name ex. `myflaskpp`

### Step 2
- Go to Your Project Folder. Open CMD in main root of project
- Try those all command
```sh
> git init
> heroku login
> heroku git:remote -a your_app_name
> pip install gunicorn
> pip freeze > requirements.txt
```
If your cmd not found `git` and `heroku` download from here

- Download Git: https://git-scm.com/downloads
- Download Heroko CLI: https://devcenter.heroku.com/articles/heroku-cli

##### Content for `requirements.txt` 
You can use this requirements.txt if you already generated requirements.txt command but still your site deplyed but getting application error.
```txt
appdirs==1.4.4
blinker==1.4
certifi==2021.5.30
chardet==4.0.0
click==8.0.1
colorama==0.4.4
distlib==0.3.2
filelock==3.0.12
Flask==2.0.1
Flask-Mail==0.9.1
Flask-MySQLdb==0.2.0
idna==2.10
itsdangerous==2.0.1
Jinja2==3.0.1
MarkupSafe==2.0.1
mysql-connector-python==8.0.25
mysqlclient==2.0.3
protobuf==3.17.3
requests==2.25.1
six==1.16.0
tabulate==0.8.9
urllib3==1.26.5
virtualenv==20.4.7
Werkzeug==2.0.1
```

### Step 3  `importent`
- Create Procfile insert this text inside file
<b>Procfile</b>
```sh
web: gunicorn app:app
```

### Step 4 `importent`
- runtime.txt insert your current python version
<b>runtime.txt </b>
```sh
python-3.9.5
```

### Step 5
Now try those command
```sh
> git add .
> git commit -m "first commit"
> git push heroku master
```
Site published but still not runing, try this command to know problem
```sh
> heroku logs --tail
```
#### Congratulations, Successfully Deployed
