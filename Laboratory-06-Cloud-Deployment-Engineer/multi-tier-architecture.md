# Two-Tier Architecture

A **two-tier architecture** splits an application into two separate layers that communicate over a network: a web/application tier that users interact with, and a database tier that stores the data. In this mission, Nextcloud is the web/application tier and MariaDB is the database tier.

## The Web/Application Tier
The web/application tier is the part of the system that users interact with. Its role is to serve the user interface, handle HTTP requests from browsers, run the application logic (such as logging in, uploading, and sharing files), and communicate with the database to read and write data. In this project, the **Nextcloud container** performs this role and is exposed to the user on port 8080.

## The Database Tier
The database tier is responsible for storing persistent data. Its role is to keep user accounts, credentials, and file metadata safe and organized, and to answer queries from the application tier. In this project, the **MariaDB container** performs this role and is only reached by the Nextcloud container.

## Why Separate Them?
Separating the web server and the database into two containers lets each tier be updated, restarted, scaled, and troubleshot independently without affecting the other. It also improves security, because the database does not need to be exposed to the public, and it follows the principle that each container should do one job well. Packing both into one container would make the system harder to maintain, scale, and debug.
