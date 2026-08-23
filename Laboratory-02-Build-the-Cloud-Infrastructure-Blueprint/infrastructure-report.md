# Infrastructure Report

## 1. System Information

| Information | Result |
|---|---|
| Operating System | Ubuntu 24.04.4 LTS |
| Kernel Version | 6.8.0-138-generic |
| CPU Model | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| Number of CPU Cores | 1 |
| Total RAM | 1.9 GiB |
| Hostname | ubuntu |

### Explanation

The KillerCoda server is running Ubuntu 24.04.4 LTS with Linux kernel version 6.8.0-138-generic. The server has one CPU core and approximately 1.9 GiB of RAM. Its hostname is ubuntu.

## 2. Network Information

| Information | Result |
|---|---|
| Main Network Interface | enp1s0 |
| Network Status | UP |
| IPv4 Address | 172.30.1.2/24 |
| Loopback Interface | lo - 127.0.0.1/8 |
| Docker Network | docker0 - 172.17.0.1/16 |

### Explanation

The main network interface is enp1s0. It is active and has the IPv4 address 172.30.1.2/24. The server also has a loopback interface and a Docker network interface.

## 3. Storage Information

| Filesystem | Type | Size | Used | Available | Usage | Mount Point |
|---|---|---:|---:|---:|---:|---|
| /dev/vda1 | ext4 | 19G | 5.4G | 13G | 30% | / |
| /dev/vda16 | ext4 | 881M | 117M | 703M | 15% | /boot |
| /dev/vda15 | vfat | 105M | 6.2M | 99M | 6% | /boot/efi |

### Explanation

The main storage filesystem is /dev/vda1. It uses the ext4 filesystem and has a capacity of 19 GB. It currently uses 5.4 GB and has approximately 13 GB available.

## 4. Mounted File Systems

The KillerCoda server contains several mounted filesystems. The main filesystem is /dev/vda1 mounted at /. There are also filesystems mounted at /boot and /boot/efi, along with temporary filesystems used by the Linux environment.

## 5. Summary

The KillerCoda environment is a Linux-based cloud server running Ubuntu 24.04.4 LTS. It provides compute resources through one CPU core and 1.9 GiB of RAM, storage through a 19 GB main filesystem, and networking through the enp1s0 interface. These resources demonstrate the basic infrastructure components used in cloud computing.
