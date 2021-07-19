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
