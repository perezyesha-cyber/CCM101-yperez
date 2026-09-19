# Laboratory 04 – Cloud-Native Engineer

## Mission Overview

This laboratory activity focused on understanding the difference between Virtual Machines and Containers. I used the KillerCoda Ubuntu environment to practice Docker commands and deploy an Nginx web server in a container.

## Objectives

- Differentiate Virtual Machines from Containers.
- Verify that Docker is installed and running.
- Pull and run an Nginx container.
- Manage the lifecycle of a Docker container.
- Document Docker operations using Markdown.
- Organize the laboratory outputs in GitHub.

## Docker Commands Executed

### Check Docker Installation

```bash
docker --version
```

### Check Docker Environment

```bash
docker info
```

### Pull Nginx Image

```bash
docker pull nginx
```

### Run Nginx Container

```bash
docker run -d -p 8080:80 --name nginx-server nginx
```

### Test Nginx Web Server

```bash
curl http://localhost:8080
```

### List Running Containers

```bash
docker ps
```

### Stop the Container

```bash
docker stop nginx-server
```

### Remove the Container

```bash
docker rm nginx-server
```

## Skills Learned

- Basic Docker command-line operations
- Container deployment and management
- Port mapping
- Nginx container deployment
- Container lifecycle management
- Technical documentation using Markdown
- Organizing cloud computing laboratory work using GitHub

## Challenges Encountered

One challenge I encountered was understanding how Docker containers use port mapping to make the Nginx web server accessible. I also had to become familiar with the Docker commands for stopping and removing containers. By following each step and checking the terminal output, I was able to complete the container deployment and lifecycle tasks successfully.
