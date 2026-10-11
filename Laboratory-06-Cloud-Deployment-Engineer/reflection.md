# Mission 6 Reflection

Writing a docker-compose.yml file makes a cloud engineer's job easier because the whole environment is described in one readable file instead of many long commands typed by hand. With docker run, I would have to remember every port, variable, and network option for each container, and one typo could break the setup. With Compose, a single command starts the entire stack the same way every time, and the file can be stored in GitHub, reviewed, and reused.

If there is an indentation error in a YAML file, such as using a Tab instead of spaces, Docker Compose cannot read the file and shows an error instead of deploying. YAML uses indentation to define structure, and tabs are not allowed, so services, images, and settings would no longer be nested correctly.

We used environment variables like MYSQL_PASSWORD to pass configuration into the containers without changing the images. They let MariaDB create its database and user, and they let Nextcloud know how to connect to it. In a real project, passwords should be stored more securely than plain text in the file.

Deploying a fully functional enterprise cloud storage system in just a few minutes felt surprising and exciting. Something that would normally require installing and configuring a web server, PHP, and a database was running after one command and a short wait. It showed me how powerful containers and automation are.

My understanding of cloud computing has grown a lot since Mission 1. At first, I thought the cloud was mainly about renting remote servers and storage. Now I understand it also involves containers, automation, and Infrastructure as Code, where infrastructure is written, versioned, and deployed like software. I now see why a senior engineer writes code instead of typing commands.
