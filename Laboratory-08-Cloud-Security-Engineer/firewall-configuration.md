# UFW Firewall Configuration Documentation

## Laboratory 08 - Cloud Security Engineer

### Purpose

The purpose of this configuration is to control incoming network connections to an Ubuntu server. UFW is used to establish security rules while keeping the services needed for remote administration and web access available.

## 1. Allow Remote Administration

Command:

```bash
sudo ufw allow ssh
```

SSH uses port 22 and allows administrators to manage the server remotely. Adding this rule before activating the firewall helps prevent accidental loss of remote access.

## 2. Establish Default Security Policies

Commands:

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

The first command rejects incoming connections that do not match an allow rule. The second command permits the server to initiate outgoing network communications.

## 3. Activate Firewall Protection

Commands:

```bash
sudo ufw enable
sudo ufw status verbose
```

The enable command starts UFW protection, while the status command displays the active policies and firewall rules.

## 4. Permit the Web Application

Command:

```bash
sudo ufw allow 8080/tcp
```

This rule permits incoming TCP connections to port 8080, which is used by the Nginx application in this laboratory.

## 5. Review Firewall Rules

Command:

```bash
sudo ufw status numbered
```

This displays the firewall rules with corresponding numbers so administrators can review the configured access permissions.

## 6. Verify Application Response

Command:

```bash
curl http://localhost:8080
```

A successful response confirms that the application is responding to requests from the local machine.

## Important Security Precaution

If `sudo ufw enable` is executed before `sudo ufw allow ssh`, the firewall may block remote SSH connections and prevent the administrator from accessing the server.

## Additional Security Consideration

A successful localhost request does not confirm that external firewall filtering is working. Docker networking can also require additional firewall controls to protect published container ports.

## Summary

UFW provides a convenient way to manage network access on Ubuntu. Allowing necessary services and restricting unnecessary connections supports safer server administration.
