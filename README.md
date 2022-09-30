# NestJS starter project

## Description

A simple REST API starter project using [Nest](https://github.com/nestjs/nest) framework.

The purpose of this project was not only to build a starter project to ease and speed up REST API creation, but also a nice opportunity to learn a new
Node.js framework.

This project is dockerized and uses PostgreSQL as the database. The app has single endpoint for health check, which checks if the database is up or not.
Naturally all the other project functionalities needs to be coded, but this helps to get started.

This app doesn't have authentication built in, but there will be another starter project with authentication.

## Environment file

The project root has `.env.template` file, which lists the needed environment files. Create a new `.env` file with the variables you need.

## Usage

This project can be started using either the default compose file (both app and db dockerized) or by using database specific compose file.

### Default compose file

Using the default `docker-compose.yml` the project is started with both application and database running in docker containers. As stated in the comments
of the `.env.template` file: when using this file to get the project up, set the database container name to the `DATABASE_HOST` environment variable
(by default it is named `db`).

### Database specific compose file

Using the `docker-compose-db.yml` only the database is running in a docker container. With this approach the node project is started locally, and the
`DATABASE_HOST` environment variable must be set as `localhost`.

```bash
# Install packages
$ yarn install

# Run project
$ yarn run start

# Run project in watch mode
$ yarn run start:dev
```
