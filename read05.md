# HEROKU
![](https://logos-download.com/wp-content/uploads/2016/09/Heroku_logo.png)

Heroku is a platform as a service (PaaS) that enables developers to build, run, and operate applications entirely in the cloud.

## Set up

First of all we have to install the Heroku Command Line Interface (CLI).

We use the CLI to manage and scale your applications, provision add-ons, view your application logs, and run your application locally.

`$sudo snap install heroku --classic`

When installation completes, we can use the heroku command from your terminal.

We will use `heroku login` command to log in to the Heroku CLI:
```
heroku login
heroku: Press any key to open up the browser to login or q to exit
 ›   Warning: If browser does not open, visit
 ›   https://cli-auth.heroku.com/auth/browser/***
heroku: Waiting for login...
Logging in... done
Logged in as me@example.com
```
This command opens the web browser to the Heroku login page. If the browser is already logged in to Heroku, simply we will click the Log in button displayed on the page.

## Create an application on Heroku

First of all we should have our repo on gitHub. Then we will run the command:

`$ heroku create`

This will create our app on Heroku it prepares heroku to receive our source code, it also generates two links for us:

```
Creating app... done, ⬢ fakestuff-farboo-84560
https://fakestuff-farboo-84560.herokuapp.com/ | https://git.heroku.com/fakestuff-farboo-84560.git

```

## Set the node server configuration

```
$ heroku config:set NPM_CONFIG_PRODUCTION=false
```

This command install the devDependencies on Heroku. More precisely, it will skip the pruning step and accesses the packages declared under devDependencies at runtime. This enables Heroku to launch npm run build.

## Listen to the Host 0.0.0.0

```
$ heroku config:set HOST=0.0.0.0

```

## Run Node in Production Mode

```
$ heroku config:set NODE_ENV=production

```

##  “npm run build”

Here we will add a script in our package json file to run (npm run build). we will add  `“heroku-postbuild”: “npm run build”` to the “script” object in our package.json:

```
"scripts": {
  "dev": "nuxt",
  "build": "nuxt build",
  "start": "nuxt start",
  "generate": "nuxt generate",
  "lint": "eslint --ext .js,.vue --ignore-path .gitignore .",
  "heroku-postbuild": "npm run build"
}
```

## Create a Procfile for Heroku

Heroku needs a Profile to execute and run our application.

`web: npm run start`

npm run start is the script that fires the application, and web directs HTTP traffic to it.

## Push the GitHub Repo to Heroku

```
$ git add Procfile
$ git commit -a -m "Configuration to deploy to heroku"
$ git push heroku master
```

And now we will have the app deployed on Heroku.

