## Purpose

Instructions to generate a new rails app.

### Choose your app name

```sh
$ APP_NAME=app-name
```

### Clone this Git repo

```sh
$ git clone git@github.com:patrykk21/rails-generator.git $APP_NAME
```

### Delete the .git folder

```sh
rm -rf .git
```

### Generate the Rails app

```sh
$ cd ..
$ rails new $(APP_NAME) -d postgresql -MCT --skip-active-job --skip-active-storage --skip-webpack-install
```
