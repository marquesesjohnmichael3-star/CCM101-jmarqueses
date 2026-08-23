# Cloud Infrastructure Components

## 1. Compute Resources

### Purpose

Compute resources provide the processing power needed to run applications, commands, services, and workloads.

### Importance in Cloud Computing

Compute resources are important because applications need CPU and memory to process tasks. Cloud providers allow organizations to increase or decrease computing resources depending on their workload.

### KillerCoda Example

The KillerCoda environment provides one CPU core using an Intel Xeon E312xx processor and approximately 1.9 GiB of RAM. These resources allow the Linux server to execute commands and run cloud-related tasks.

---

## 2. Storage Resources

### Purpose

Storage resources are used to store the operating system, applications, configuration files, and data.

### Importance in Cloud Computing

Storage is important because applications and users need a reliable place to save data. Cloud platforms provide storage that can be expanded when more capacity is needed.

### KillerCoda Example

The KillerCoda server has a main filesystem named /dev/vda1. It uses the ext4 filesystem and has a capacity of 19 GB, with approximately 13 GB available.

---

## 3. Networking Resources

### Purpose

Networking resources allow computers, applications, and users to communicate with each other.

### Importance in Cloud Computing

Networking is important because cloud services need communication between users, servers, applications, and other resources.

### KillerCoda Example

The main network interface in KillerCoda is enp1s0. It is active and uses the IPv4 address 172.30.1.2/24. The environment also contains a Docker network interface named docker0.

---

## 4. Operating System

### Purpose

The operating system manages hardware resources and provides an environment where applications and commands can run.

### Importance in Cloud Computing

Operating systems are important because cloud virtual machines need an operating system to manage resources and run applications and services.

### KillerCoda Example

The KillerCoda environment uses Ubuntu 24.04.4 LTS with Linux kernel version 6.8.0-138-generic. Linux provides the command-line environment used to inspect and manage the server.

---

## Conclusion

The KillerCoda environment demonstrates how compute, storage, networking, and the operating system work together. The CPU and RAM provide computing power, storage keeps system files and data, networking provides connectivity, and Ubuntu Linux manages the server resources.
