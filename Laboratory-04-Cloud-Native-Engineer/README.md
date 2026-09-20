# Laboratory 04 - Cloud-Native Engineer

## Mission Overview

This laboratory activity introduced containerization and the use of Docker in a cloud-native environment. I used the KillerCoda Docker Playground to verify Docker, download the Nginx image, run a containerized web server, test it through port 8080, and manage the container lifecycle.

## Objectives

- Understand the difference between Virtual Machines and Containers.
- Access a Docker-enabled cloud environment using KillerCoda.
- Execute basic Docker CLI commands.
- Pull and run an Nginx container.
- Manage the lifecycle of a Docker container.
- Document cloud-native operations using Markdown.
- Continue developing my GitHub Cloud Computing portfolio.

## Docker Commands Executed

### Verify Docker

docker --version
docker info

### Download the Nginx Image

docker pull nginx

### Run the Nginx Container

docker run -d --name nginx -p 8080:80 nginx

### Test the Web Server

curl http://localhost:8080

### List Running Containers

docker ps

### Stop the Container

docker stop nginx

### Verify the Container Status

docker ps -a

### Remove the Container

docker rm nginx

### Skills Learned

I learned how containers can provide a lightweight way to run applications without installing a complete operating system for each application. I also practiced using Docker commands to download images, create containers, expose ports, test services, and manage the container lifecycle. I improved my ability to document technical procedures using Markdown and GitHub.

### Challenges Encountered

One challenge was understanding the difference between a Docker image and a running container. I also had to make sure that the correct port mapping was used so that the Nginx web server could be accessed through port 8080. Managing the container through the stop and remove commands also helped me understand the Docker container lifecycle.
