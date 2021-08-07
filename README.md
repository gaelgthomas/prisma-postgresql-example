# Prisma JS with PostgreSQL example

This repository aims to share a simple example of database management using [Prisma](https://www.prisma.io/) and a PostgreSQL database.

You can find the related Twitter thread by [clicking here](https://twitter.com/gaelgthomas/status/1423993422088708099).

## Requirements to build the project

- Docker
- Node

## Build the project

1. Launch the docker-compose to build and create a default database.

```
$ docker-compose up
```

Here are the default credentials:

```
POSTGRES_USER: username
POSTGRES_PASSWORD: password
POSTGRES_DB: default_database
```

> **Note:** the project is pre-configured with these credentials. Please update them in the `docker-compose.yml` and `.env` files if you want to change them.

2. Run the migration with Prisma (initialize the database).

```
$ npx prisma migrate dev --name init
```

## Launch the project

You can run the default queries by launching the `script.ts` file.
This script will create a user and its first tweet. Then, it will fetch the user with all its tweets and display them.

```
$ npm run dev
```
