# Laboratory 03 – Multi-Cloud Explorer

## Mission Overview

This laboratory activity explored AWS, Microsoft Azure, and Google Cloud Platform. It focused on researching cloud services, comparing cloud platforms, analyzing business scenarios, and connecting Linux infrastructure with cloud computing services.

## Linux Investigation

The Linux server was investigated using commands in the KillerCoda Playground.

### Operating System

**Operating System:** Ubuntu 24.04.4 LTS

**Kernel Version:** 6.8.0-138-generic

### CPU Information

**CPU:** Intel Xeon E312xx (Sandy Bridge, IBRS update)

**CPU Cores:** 1

### Memory

**Total Memory:** 1.9 GiB

**Used Memory:** 409 MiB

**Free Memory:** 873 MiB

**Available Memory:** 1.5 GiB

**Swap:** 1.0 GiB

### Disk Space

**Root Filesystem:** 19 GiB total, 5.4 GiB used, 13 GiB available, 30% used

**Boot Filesystem:** 881 MiB total, 117 MiB used, 703 MiB available, 15% used

**EFI Filesystem:** 105 MiB total, 6.2 MiB used, 99 MiB available, 6% used

### Network Information

**Hostname:** ubuntu

**Network Interface:** enp1s0

**Status:** UP

**IPv4 Address:** 172.30.1.2/24

## Possible Cloud Services

### AWS

The Linux server could be hosted using Amazon EC2, which provides virtual servers for running applications and operating systems.

### Microsoft Azure

The Linux server could be hosted using Azure Virtual Machines, which supports Linux virtual machines and cloud workloads.

### Google Cloud

The Linux server could be hosted using Compute Engine, which provides virtual machines running on Google Cloud infrastructure.

## Linux Commands Used

```bash
cat /etc/os-release
uname -r
lscpu
free -h
df -h
ip addr
hostname
