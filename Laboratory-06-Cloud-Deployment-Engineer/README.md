# Laboratory 06: The Cloud Deployment Engineer

## Mission Overview
In this mission, I joined the Cloud Deployment Team at CloudNova Technologies and moved from deploying single containers to deploying a multi-tier application using Docker Compose. I defined a two-tier private cloud storage system (Nextcloud web application + MariaDB database) as Infrastructure as Code (IaC) in a `docker-compose.yml` file and deployed the whole stack with a single command.

## Objectives
- Explain the concept of a multi-tier application architecture.
- Understand the purpose and structure of a `docker-compose.yml` file.
- Use a Linux command-line text editor (nano) to create configuration files.
- Deploy a multi-container application (Nextcloud + MariaDB) using Docker Compose.
- Document deployment procedures and IaC principles using Markdown.
- Continue expanding my GitHub Cloud Computing Portfolio.

## Commands Executed
```bash
git clone https://github.com/marquesesjohnmichael3-star/CCM101-jmarqueses.git   # clone portfolio repo
mkdir nextcloud-deployment        # create project directory
cd nextcloud-deployment           # move into the directory
nano docker-compose.yml           # create the Compose file
docker-compose up -d              # deploy the multi-container stack in the background
docker-compose ps                 # verify both containers are running
docker-compose down               # stop and remove the stack
git add .                         # stage all files
git commit -m "Add Laboratory 06 - Cloud Deployment Engineer"   # commit changes
git push                          # push to GitHub
```

## Screenshots
| Evidence | File |
|---|---|
| Successful deployment and running containers | `screenshots/compose-deployment.png` |
| Nextcloud installation page in the browser (port 8080) | `screenshots/nextcloud-web.png` |
| Containers stopped and removed | `screenshots/compose-teardown.png` |

## Skills Learned
- Understanding two-tier (multi-tier) architecture
- Writing YAML configuration files with correct indentation
- Using the nano text editor in the Linux terminal
- Deploying and tearing down multi-container applications with Docker Compose
- Linking containers using service names and environment variables
- Exposing an application through port mapping (8080:80)
- Documenting Infrastructure as Code using Markdown
- Managing a GitHub portfolio repository
