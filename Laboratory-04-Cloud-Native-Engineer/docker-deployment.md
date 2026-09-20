# Docker Deployment

## 1. Verify Docker

### Command

docker --version

This command displays the installed Docker version and confirms that the Docker CLI is available.

### Command

docker info

This command displays information about the Docker environment and confirms that the Docker daemon is responding.

## 2. Download the Nginx Image

### Command

docker pull nginx

This command downloads the official Nginx image from Docker Hub to the local Docker environment.

## 3. Run the Nginx Container

### Command

docker run -d --name nginx -p 8080:80 nginx

This command creates and starts an Nginx container in detached mode while mapping host port 8080 to container port 80.

## 4. Test the Web Server

### Command

curl http://localhost:8080

This command sends a local HTTP request to the Nginx server and displays its HTML response.

## 5. List Running Containers

### Command

docker ps

This command displays the containers that are currently running.

## 6. Stop the Container

### Command

docker stop nginx

This command stops the running Nginx container.

## 7. Verify the Container Is Stopped

### Command

docker ps -a

This command displays all containers, including the stopped Nginx container.

## 8. Remove the Container

### Command

docker rm nginx

This command permanently removes the stopped Nginx container from the Docker environment.

## Container Lifecycle Summary

The Docker container lifecycle used in this activity was:

Docker Image
     ↓
docker run
     ↓
Running Container
     ↓
docker stop
     ↓
Stopped Container
     ↓
docker rm
     ↓
Container Removed

## Port Mapping

The Nginx container uses port 80 internally. The command -p 8080:80 connects port 8080 on the host to port 80 inside the container, allowing the Nginx service to be accessed through localhost:8080.
