## Purpose

Instructions to generate a new rails app.

### Choose your app name

```sh
$ APP_NAME=app-name
```

### Clone this Git repo

```sh
$ git clone git@github.com:patrykk21/rails-generator.git
```

### Rename the directory

```sh
$ cd ..
$ mv rails-generator $(APP_NAME)
```

### Delete the .git folder

```sh
rm -rf $(APP_NAME)/.git
```

### Generate the Rails app

```sh
$ rails new $(APP_NAME) -d postgresql -MCT --skip-active-job --skip-active-storage --skip-webpack-install
```
