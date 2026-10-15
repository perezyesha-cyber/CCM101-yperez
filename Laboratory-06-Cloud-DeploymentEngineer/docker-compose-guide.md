# Docker Compose Guide

## What Does the `services:` Block Do?

The `services:` block defines the containers needed for an application. In this laboratory, it contains two services: `database` and `app`. The database service uses MariaDB, while the app service uses Nextcloud.

## How Does Nextcloud Find the Database?

Nextcloud finds the database through the `MYSQL_HOST=database` environment variable. The name `database` matches the database service defined in the Docker Compose file. Docker Compose provides a network that allows the two containers to communicate with each other.

## Difference Between `docker run` and `docker-compose up -d`

The `docker run` command starts an individual container using the options provided in the command. In contrast, `docker-compose up -d` uses a YAML configuration file to create and start multiple related containers together in the background. Docker Compose makes it easier to manage applications with multiple services.

## Conclusion

Docker Compose simplifies the deployment of multi-container applications. By using a configuration file, cloud engineers can organize, deploy, and manage application services more efficiently.
