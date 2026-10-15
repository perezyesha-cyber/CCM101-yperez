# Laboratory 06 – Cloud Deployment Engineer

## Mission Overview

This laboratory activity focuses on deploying a private cloud storage application using Docker Compose. I deployed Nextcloud as the web application and MariaDB as its database.

## Objectives

- Understand two-tier application architecture.
- Create a Docker Compose YAML configuration file.
- Deploy Nextcloud and MariaDB containers.
- Access the Nextcloud web interface through port 8080.
- Document the deployment process using Markdown.

## Commands Executed

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
cat docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Skills Learned

- Understanding multi-tier architecture.
- Creating YAML configuration files using nano.
- Deploying multiple containers using Docker Compose.
- Connecting an application container to a database container.
- Accessing a web application through a browser.
- Documenting cloud deployment activities using Markdown.
- Understanding Infrastructure as Code (IaC).



