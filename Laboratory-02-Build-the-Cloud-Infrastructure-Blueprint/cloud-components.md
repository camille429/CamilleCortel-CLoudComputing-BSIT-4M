# Cloud Infrastructure Components

This document identifies and explains the core infrastructure components found in the KillerCoda Linux cloud environment.

---

## 1. Compute Resources
- **Purpose:** Provides processing power (CPU cores and memory) to run applications, process data, and execute instructions. It serves as the "brain" of any cloud system.
- **Importance in Cloud Computing:** Without compute resources, no workloads or services can run. It determines how fast and how many tasks a cloud server can handle at the same time.
- **Relation to KillerCoda Environment:** The virtual CPU cores and allocated memory assigned to this Linux server are the compute resources that power the terminal and all commands executed.

---

## 2. Storage Resources
- **Purpose:** Stores the operating system, installed applications, files, and data persistently so they remain available even when the system restarts.
- **Importance in Cloud Computing:** Ensures that data is saved, retrievable, and durable. Every cloud service needs storage to keep its state and user information safe.
- **Relation to KillerCoda Environment:** The 20GB virtual disk (`vda`) and its partitions (`/`, `/boot`) are the storage where Ubuntu and all system files are kept.

---

## 3. Networking Resources
- **Purpose:** Enables communication between the server, the internet, and other systems. It includes IP addresses, network interfaces, and connection rules.
- **Importance in Cloud Computing:** Allows users to access cloud services and lets different cloud components talk to each other. Without networking, the cloud would be isolated and useless.
- **Relation to KillerCoda Environment:** The IP address `172.30.1.2` and network interface `ens190` are what connect this Linux server to the internet and allow us to access it through the browser.

---

## 4. Operating System
- **Purpose:** Manages all hardware and resources, provides a layer between the user and the physical/virtual machine, and allows software and applications to run.
- **Importance in Cloud Computing:** Acts as the foundation layer. Almost all cloud servers run on Linux because it is stable, secure, lightweight, and highly customizable.
- **Relation to KillerCoda Environment:** Ubuntu 24.04.4 LTS is the operating system that controls the CPU, RAM, Disk, and Network — and lets us run commands in the terminal.
