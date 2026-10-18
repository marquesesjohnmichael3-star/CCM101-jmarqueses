# Security Audit Report

## Laboratory Activity 8 - Cloud Security Engineer

### 1. Principle of Least Privilege (PoLP)

The Principle of Least Privilege is a security practice where each user or system process receives only the access required for its assigned responsibilities. In a cloud environment, this prevents unnecessary permissions from being misused and limits the impact of compromised accounts.

### 2. Attack Surface

The attack surface of a virtual machine consists of the network services, accounts, applications, and interfaces that attackers might attempt to exploit. Reducing unnecessary services and restricting exposed ports can make a server more difficult to attack.

### 3. Default Deny Policy

A Default Deny Policy rejects incoming connections unless an administrator has created a rule that explicitly permits them. It provides stronger protection because unfamiliar or unexpected connections are blocked automatically instead of depending on a list of known threats.

## Security Audit Procedure

The Ubuntu server will be inspected using the following command:

```bash
sudo ss -tuln
```

This command lists listening TCP and UDP ports, helping identify network services that may require firewall restrictions.

## Security Goal

The server should permit SSH administration on port 22 and application access on TCP port 8080 while denying other incoming connections by default.
