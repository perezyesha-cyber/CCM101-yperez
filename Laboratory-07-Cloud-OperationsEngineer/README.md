# Laboratory 07 – Cloud Operations Engineer

## Mission Overview

This laboratory activity focuses on monitoring a Linux server and a Docker container. I used KillerCoda to check the host system's resources, deploy an Nginx web server, generate HTTP requests, examine application logs, and monitor container performance.

## Objectives

- Check the host server's memory and disk capacity.
- Deploy an Nginx web server using Docker.
- Generate three successful HTTP requests and one request to a missing page.
- Retrieve application logs and identify the HTTP 404 error.
- Monitor CPU, memory, and network usage using Docker.
- Document the results and improve my troubleshooting skills.

## Monitoring Commands Executed

| Command | Purpose |
|---|---|
| `free -h` | Checks the server's memory usage. |
| `df -h /` | Checks the available disk space on the root filesystem. |
| `top` | Displays running processes and CPU activity. |
| `docker run -d --name clientwebsite -p 8080:80 nginx` | Deploys the Nginx container in the background. |
| `docker ps` | Displays running Docker containers. |
| `curl http://localhost:8080` | Sends an HTTP request to the website. |
| `curl http://localhost:8080/hidden-admin-page` | Tests a missing page and generates a 404 response. |
| `docker logs clientwebsite` | Displays application and access logs for troubleshooting. |
| `docker stats` | Monitors container resource usage in real time. |

## Skills Learned

In this activity, I learned how to check Linux server resources, deploy a web server using Docker, generate HTTP traffic, identify a 404 error, and examine application logs. I also learned how to monitor CPU, memory, and network usage. These skills helped me understand how monitoring and troubleshooting support reliable cloud operations.
