# Docker Compose Guide

This guide explains the `docker-compose.yml` file used to deploy a private Nextcloud cloud storage system.

## The Code
```yaml
version: '3'

services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - 8080:80
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
```

## What does the `services:` block do?
The `services:` block defines every container that makes up the application. Each entry under it (`database` and `app`) is one service, and each service has its own image, environment variables, and ports. Docker Compose reads this block to know which containers to create, how to configure them, and how to start them together. It also places all services on a shared network automatically.

## How did the Nextcloud app container know how to find the database container?
The Nextcloud container found the database through the `MYSQL_HOST=database` environment variable. The value `database` is the **name of the database service** in the Compose file. Docker Compose creates a default network for the stack and provides built-in DNS, so each service name resolves to that container's IP address. Nextcloud therefore connects to `database` without needing a hardcoded IP address. The matching `MYSQL_USER`, `MYSQL_PASSWORD`, and `MYSQL_DATABASE` values let it log in to the MariaDB database.

## What is the difference between `docker run` and `docker-compose up -d`?
| `docker run` | `docker-compose up -d` |
|---|---|
| Starts **one** container per command | Starts **all** services defined in the file with one command |
| Options (ports, variables, networks) are typed manually each time | Configuration is saved in a `docker-compose.yml` file |
| Linking containers requires manual networking setup | Creates a shared network automatically |
| Harder to repeat and prone to typing errors | Repeatable and version-controllable (Infrastructure as Code) |

The `-d` flag runs the containers in **detached mode**, meaning in the background, so the terminal stays free.
