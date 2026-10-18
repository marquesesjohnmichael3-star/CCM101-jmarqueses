
# Laboratory Activity 7: The Cloud Operations Engineer

## Mission Overview

This activity focuses on checking system resources and observing a running web service. An Nginx container was deployed and tested to examine how request results, container logs, and resource metrics support basic cloud operations.

## Objectives

- Record the Ubuntu environment's memory and disk capacity.
- Launch an Nginx container named `client-website`.
- Test valid requests and a request to a nonexistent page.
- Review container logs and identify the 404 response.
- Observe memory usage, CPU percentage, and network I/O.

## Monitoring Commands Executed

| Command | Purpose |
|---|---|
| `free -h` | Check memory and swap information |
| `df -h /` | Check root filesystem capacity |
| `top` | Observe running processes |
| `docker ps` | Check container status |
| `curl -i http://localhost:8080/` | Test the Nginx homepage |
| `curl -i http://localhost:8080/hidden-admin-page` | Test a nonexistent path |
| `docker logs client-website` | Inspect container logs |
| `docker stats client-website` | Observe live resource usage |

## Skills Learned

This activity provided practice in reading Linux resource information, starting a containerized web server, testing HTTP responses, and interpreting Docker logs and metrics. It also demonstrated how different monitoring commands can help an operator investigate a web service.

## Screenshots

The following evidence should be added to the `screenshots/` folder:

- `memory-check.png`
- `disk-check.png`
- `install-nginx.png`
- `simulation1.png`
- `simulation2.png`
- `docker-logs.png`
- `container-metrics.png`
