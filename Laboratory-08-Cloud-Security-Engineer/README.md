# Laboratory 08: The Cloud Security Engineer

## Mission Overview

This activity introduces practical server protection techniques using Ubuntu, Docker, and UFW. The mission involves running an Nginx web application, examining network services, and applying firewall rules to manage which connections are permitted.

## Objectives

The objectives of this laboratory are to:

1. Identify possible network security risks on a Linux server.
2. Understand why unnecessary open ports increase security exposure.
3. Apply firewall rules using Ubuntu UFW.
4. Preserve SSH access for server administration.
5. Configure TCP port 8080 for the web application.
6. Record the security procedures and their results.

## Tools and Technologies

- KillerCoda Ubuntu Playground
- Linux Terminal
- Docker
- Nginx
- Uncomplicated Firewall (UFW)
- Curl
- Git and GitHub

## Commands Executed

### Application Deployment

```bash
docker run -d --name secure-web-app -p 8080:80 nginx:alpine
docker ps
curl http://localhost:8080
```

### Network Inspection

```bash
sudo ss -tuln
sudo ufw status verbose
```

### Firewall Setup

```bash
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
```

### Application Port Configuration

```bash
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl -I http://localhost:8080
```

## Skills Learned

Through this laboratory, I practiced identifying listening network ports, configuring Linux firewall rules, and checking the accessibility of a containerized application.

I also learned why administrators must protect SSH access before activating firewall restrictions and why security configurations should be reviewed carefully.

## Screenshot Evidence

The following screenshots document the laboratory checkpoints:

1. `screenshots/vulnerable-app-running.png` - Nginx application response.
2. `screenshots/firewall-activated.png` - UFW activation and default policies.
3. `screenshots/firewall-port-allowed.png` - Firewall rules and application test.

## Security Reminder

Docker-published ports may require additional network protection beyond standard UFW rules. Local curl testing confirms application response but not external firewall enforcement.

## Conclusion

This mission demonstrates how firewall policies contribute to cloud infrastructure security. By managing incoming connections and reviewing exposed services, administrators can reduce unnecessary network risks.
