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
docker-compose -f docker-compose.dev.yml build app
```

### Run docker container

```sh
docker-compose -f docker-compose.dev.yml run app /bin/bash
```

#### Remove unnecessary files

```sh
rm -rf .git
rm README.md
rm Gemfile Gemfile.lock
```

#### Generate the Rails app

```sh
cd ..
rails new app -d postgresql -M -C -T --skip-active-job --skip-active-storage
```

#### Change database.yml

Add below info

```yml
host: <%= ENV.fetch("DB_HOST") { "psql" } %>
username: <%= ENV.fetch("DB_USER") { "postgres" } %>
password: <%= ENV.fetch("DB_PASS") { "postgres" } %>
```
