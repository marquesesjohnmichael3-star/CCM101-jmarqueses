# Mission 4 Reflection

This laboratory helped me understand the difference between using traditional Virtual Machines and using containers. A Virtual Machine needs to start a complete operating system before an application can run, which can take more time and use more system resources. A Docker container is much faster to start because it shares the host operating system kernel. In this activity, I was able to pull the Nginx image and run a web server in only a few commands.

The port mapping `-p 8080:80` is necessary because the Nginx service is running on port 80 inside the container. Mapping it to port 8080 allows me to access the service from the host using `http://localhost:8080`. Without the port mapping, the service would still be running inside the container, but it would not be directly accessible through the host's port 8080.

When the `docker rm` command is used, the selected stopped container is removed. The container itself and its writable container layer are deleted, so data stored only inside that container can be lost. This shows why persistent data should be stored using appropriate Docker storage methods when it needs to remain after a container is removed.

Containerization can also improve cooperation between software developers and IT operations teams. Developers can package an application together with its required environment, while operations teams can use the same container image for deployment. This can make the process more consistent from development to deployment.

My GitHub portfolio is also becoming more organized as I add different cloud computing activities. This laboratory added practical Docker experience to my previous cloud activities. It also helped me improve my technical documentation skills because I had to record commands, results, screenshots, and explanations in Markdown.
