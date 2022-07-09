## Purpose

Instructions to generate a new rails app.

### Choose your app name

```sh
APP_NAME=app-name
```

### Clone this Git repo

```sh
git clone git@github.com:patrykk21/rails-generator.git $APP_NAME
```

### Build docker image

```sh
cd $APP_NAME
docker build -t $APP_NAME -f Dockerfile.dev .
```

### Run docker container

```sh
docker run -it -v $(pwd):/app $APP_NAME /bin/bash
```

### Delete the .git folder

```sh
rm -rf .git
```

### Generate the Rails app

```sh
cd ..
rails new app -d postgresql -MCT --skip-active-job --skip-active-storage --skip-webpack-install
```
