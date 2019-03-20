# README

## Building the Rails app docker image
Before Building the Dockerfile you need to create a .env file in your app folder same as the .env.test file that stores environments for your development environement.

```shell
cp app/.env.test app/.env
```

First time you run this app and also each time you add a new Gem to your code you need to build the docker image.

```shell
docker-compose stop
docker-compose build
````

## Running the Rails app
You should only run the below command once you have build the image in the previous step.

```shell
docker-compose start
```
Accessing the Application:
http://docker-host:3000 (http://localhost:3000)

## Running the rails app minitests
The below command is equivalent to running `rails test`
```shell
docker-compose run -T test
```

## Running the rails db:migrate
The below command is equivalent to running `rails db:migrate`
```shell
docker-compose run -T db_migrate
```

## Maintainer
Anto Dominic
