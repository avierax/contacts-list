# Contacts List

This is a test application with Spring Boot as Backend and Vue.js as Frontend

## 1. Backend App

* JDK 1.8
* Spring Boot 2.1.0
* Spring Web 2.1.0
* Spring Boot JPA 2.1.0
* Spring Boot Beans Validation 2.1.0
* PostgreSQL 9.6 (Postgres is the core for [EDB Postgres](https://www.enterprisedb.com/))
* Apache Commons CSV 1.6
* Lombok 1.18
* Maven 3

## 2. Fronted App

* Javascript
* Vue.js 2.5
* Vuex 3.0
* Axios
* Vuetify 1.0
* Webpack 3.7.1
* Node.js 8.11.3
* NPM 5.6

I strongly recommend to use [Node Version Manager](https://github.com/creationix/nvm) for building the application

## 3. How to deploy the App

This solution is based on Git Repositories and contains one [Master Repository](https://github.com/oscartoledo/contacts-list) that contains two submodules [Fronted App](https://github.com/oscartoledo/contacts-view) and [Backend App](https://github.com/oscartoledo/contacts). Each project in those submodules can be deployed by itself, but I recommend to use the master repository that contains a Docker Compose based solution.

### 3.1 Requirements

To deploy the application ecosystem from Docker Compose solution you must have installed

* [Git version 2.7.4](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) You can verify this executing the command `git --version`
* You need a [GiHub Account](https://github.com/join) and associate an [SSH key](https://help.github.com/articles/connecting-to-github-with-ssh/) to your account.
* [Docker version 18.06.1-ce, build e68fc7a](https://docs.docker.com/install/) You can verify this executing the command `docker --version`
* [Docker Compose version 1.21.2, build a133471](https://docs.docker.com/compose/install/) You can verify this executing the command `docker-compose --version`

### 3.2 Steps to deploy the app on localhost (Easier way)

1. Clone the Master Repository and its submodules `git clone --recursive git@github.com:oscartoledo/contacts-list.git`
1. Go inside the Master Repository folder `cd contacts-list`
1. Build and Deploy the containers `docker-compose up` if you want detach container from terminal please use `docker-compose up -d`

### 3.3 Steps to deploy the app on a remote server

1. Clone the Master Repository and its submodules `git clone --recursive git@github.com:oscartoledo/contacts-list.git`
1. Go inside the Master Repository folder `cd contacts-list`
1. Update API address in Frontend application
1. Open the Production environment file `nano contacts-view/config/prod.env.js`
1. Update the value off BASE_URL constant, exit and save
1. Build and Deploy the containers `docker-compose up -d`
