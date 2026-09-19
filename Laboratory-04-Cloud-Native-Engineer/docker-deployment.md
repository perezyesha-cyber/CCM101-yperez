# Docker Deployment

## Container Lifecycle

### 1. List Running Containers

```bash
docker ps
```

This command lists the Docker containers that are currently running.

### 2. Stop the Running Container

```bash
docker stop nginx-server
```

This command stops the running Nginx container named `nginx-server`.

### 3. Verify the Container is Stopped

```bash
docker ps
```

This command verifies that the Nginx container is no longer running.

### 4. Remove the Container

```bash
docker rm nginx-server
```

This command removes the stopped `nginx-server` container.

## Result

The Nginx container was successfully stopped and removed after completing the container lifecycle demonstration.
