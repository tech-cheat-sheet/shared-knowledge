- [CompTIA Linux+ Exam XK0-005](#comptia-linux-exam-xk0-005)
- [1.0 System Management](#10-system-management)
  - [1.1 Summarize Linux fundamentals](#11-summarize-linux-fundamentals)
    - [📁 Filesystem Hierarchy Standard (FHS)](#-filesystem-hierarchy-standard-fhs)
    - [🧃 Basic Boot Process](#-basic-boot-process)
      - [🔧 Boot Commands](#-boot-commands)
      - [🌀 Boot Sources](#-boot-sources)
      - [💥 Kernel Panic](#-kernel-panic)
    - [⚙️ /dev Device Types](#️-dev-device-types)
    - [🔨 Package Compilation (from Source)](#-package-compilation-from-source)
  - [1.2 Given a scenario, manage files and directories](#12-given-a-scenario-manage-files-and-directories)
    - [✏️ File Editing](#️-file-editing)
    - [📦 File Compression, Archiving, and Backup](#-file-compression-archiving-and-backup)
    - [🗃️ File Metadata](#️-file-metadata)
    - [🔗 Soft and Hard Links](#-soft-and-hard-links)
    - [🌐 Copying Files Between Systems](#-copying-files-between-systems)
    - [🧱 File \& Directory Operations](#-file--directory-operations)
  - [1.3 Given a scenario, configure and manage storage using the appropriate tools](#13-given-a-scenario-configure-and-manage-storage-using-the-appropriate-tools)
    - [🔧 Disk Partitioning](#-disk-partitioning)
    - [📂 Mounting Local and Remote Devices](#-mounting-local-and-remote-devices)
    - [🧮 Filesystem Management](#-filesystem-management)
    - [📊 Monitoring Storage and Usage](#-monitoring-storage-and-usage)
    - [🧱 Logical Volume Manager (LVM)](#-logical-volume-manager-lvm)
    - [🔁 Inspecting RAID](#-inspecting-raid)
    - [🌐 SAN/NAS and Network Filesystems](#-sannas-and-network-filesystems)
    - [🔍 Storage Hardware Inspection](#-storage-hardware-inspection)
  - [1.4 Given a scenario, configure and use the appropriate processes and services](#14-given-a-scenario-configure-and-use-the-appropriate-processes-and-services)
    - [🛎️ System Services with `systemctl`](#️-system-services-with-systemctl)
    - [⏰ Scheduling Services](#-scheduling-services)
    - [🧠 Process Management](#-process-management)
      - [💥 Kill Signals](#-kill-signals)
      - [📋 Listing Processes and Open Files](#-listing-processes-and-open-files)
      - [📌 Setting Process Priorities](#-setting-process-priorities)
      - [🌡️ Process States](#️-process-states)
      - [🎮 Job Control (Terminal Jobs)](#-job-control-terminal-jobs)
      - [🔍 Searching \& Terminating Processes](#-searching--terminating-processes)
  - [1.5 Given a scenario, use the appropriate networking tools or configuration files](#15-given-a-scenario-use-the-appropriate-networking-tools-or-configuration-files)
    - [🔌 Interface Management](#-interface-management)
      - [🧰 iproute2 Tools](#-iproute2-tools)
      - [📡 NetworkManager](#-networkmanager)
      - [🔧 Legacy Net-Tools](#-legacy-net-tools)
      - [🗂️ Configuration Files](#️-configuration-files)
    - [📛 Name Resolution](#-name-resolution)
      - [🔍 DNS Tools (Bind-utils)](#-dns-tools-bind-utils)
      - [🌎 WHOIS](#-whois)
    - [📊 Network Monitoring](#-network-monitoring)
    - [📡 Remote Networking Tools](#-remote-networking-tools)
  - [1.6 Given a scenario, build and install software](#16-given-a-scenario-build-and-install-software)
    - [📦 Package Management](#-package-management)
    - [🧪 Sandboxed Applications](#-sandboxed-applications)
    - [🔄 System Updates](#-system-updates)
      - [🔧 Kernel Updates](#-kernel-updates)
      - [📥 Package Updates](#-package-updates)
  - [1.7 Given a scenario, manage software configurations](#17-given-a-scenario-manage-software-configurations)
    - [🔧 Updating Configuration Files](#-updating-configuration-files)
      - [🔄 Procedures](#-procedures)
      - [🗂️ RPM-based Config File Management](#️-rpm-based-config-file-management)
      - [📁 Repository Configuration Files](#-repository-configuration-files)
    - [🧪 Configure Kernel Options](#-configure-kernel-options)
      - [⚙️ Kernel Parameters](#️-kernel-parameters)
      - [🧩 Kernel Modules](#-kernel-modules)
    - [🛠️ Configure Common System Services](#️-configure-common-system-services)
    - [🌍 Localization Tools](#-localization-tools)
- [2.0 Security](#20-security)
  - [2.1 Summarize the purpose and use of security best practices in a Linux environment](#21-summarize-the-purpose-and-use-of-security-best-practices-in-a-linux-environment)
    - [🛡️ Public Key Infrastructure (PKI) Certificates](#️-public-key-infrastructure-pki-certificates)
    - [🔒 Certificate Use Cases](#-certificate-use-cases)
    - [👤 Authentication Technologies](#-authentication-technologies)
    - [🧱 Linux Hardening](#-linux-hardening)
      - [🔍 Security Measures](#-security-measures)
      - [⚙️ System Configuration](#️-system-configuration)
  - [2.2 Given a scenario, implement identity management](#22-given-a-scenario-implement-identity-management)
    - [👤 Account Creation and Deletion](#-account-creation-and-deletion)
    - [🐚 Default Shell and Skeleton Files](#-default-shell-and-skeleton-files)
    - [🗄️ Configuration Files](#️-configuration-files-1)
    - [🔐 Account Management Tools](#-account-management-tools)
  - [2.3 Given a scenario, implement and configure firewalls](#23-given-a-scenario-implement-and-configure-firewalls)
    - [🎯 Firewall Use Cases](#-firewall-use-cases)
    - [🛠️ Common Firewall Technologies](#️-common-firewall-technologies)
      - [🔹 firewalld](#-firewalld)
      - [🔹 iptables](#-iptables)
      - [🔹 nftables](#-nftables)
      - [🔹 UFW (Uncomplicated Firewall)](#-ufw-uncomplicated-firewall)
      - [🔐 Key Firewall Features](#-key-firewall-features)
  - [2.4 Given a scenario, configure and execute remote connectivity for system management](#24-given-a-scenario-configure-and-execute-remote-connectivity-for-system-management)
    - [🔐 SSH Configuration Files](#-ssh-configuration-files)
    - [🔑 SSH Commands](#-ssh-commands)
      - [Example Workflow:](#example-workflow)
    - [🔀 SSH Tunneling Techniques](#-ssh-tunneling-techniques)
      - [👥 Executing Commands as Another User](#-executing-commands-as-another-user)
      - [🔧 Configuration Files](#-configuration-files)
      - [🛠️ Common Privilege-Elevation Commands](#️-common-privilege-elevation-commands)
      - [Example Usage:](#example-usage)
  - [2.5 Given a scenario, apply the appropriate access controls](#25-given-a-scenario-apply-the-appropriate-access-controls)
    - [📁 File Permissions](#-file-permissions)
      - [🔧 Extended Attributes](#-extended-attributes)
      - [Example:](#example)
    - [🛡️ SELinux (Security-Enhanced Linux)](#️-selinux-security-enhanced-linux)
      - [📦 Context \& Label Management](#-context--label-management)
      - [📋 SELinux States](#-selinux-states)
      - [🔁 System Booleans](#-system-booleans)
        - [Example:](#example-1)
      - [🔐 Policy Types](#-policy-types)
- [3.0 3.0 Scripting, Containers, and Automation](#30-30-scripting-containers-and-automation)
  - [3.1 Given a scenario, create simple shell scripts to automate common tasks](#31-given-a-scenario-create-simple-shell-scripts-to-automate-common-tasks)
    - [🔁 Loops](#-loops)
    - [🔀 Conditionals](#-conditionals)
    - [🧪 Parameter Expansion \& Patterns](#-parameter-expansion--patterns)
    - [🔢 Comparisons](#-comparisons)
    - [📦 Variables \& Input](#-variables--input)
    - [🔄 Search and Replace](#-search-and-replace)
    - [📊 Standard Stream Redirection](#-standard-stream-redirection)
        - [Here Document Example:](#here-document-example)
      - [🚪 Exit Codes](#-exit-codes)
      - [🧰 Built-In and Utility Commands](#-built-in-and-utility-commands)
      - [🌍 Environment Variables](#-environment-variables)
        - [Example Usage:](#example-usage-1)
      - [🗂️ File Path Types](#️-file-path-types)
  - [3.2 Given a scenario, perform basic container operations](#32-given-a-scenario-perform-basic-container-operations)
    - [🛠️ Container Management](#️-container-management)
    - [🖼️ Container Image Operations](#️-container-image-operations)
    - [🧪 Example Workflow: Simple Web Container](#-example-workflow-simple-web-container)
  - [3.3 Given a scenario, perform basic version control using Git](#33-given-a-scenario-perform-basic-version-control-using-git)
    - [🔃 Cloning Repositories](#-cloning-repositories)
    - [📤 Pushing and 📥 Pulling Changes](#-pushing-and--pulling-changes)
    - [✍️ Staging and Committing Changes](#️-staging-and-committing-changes)
    - [🚀 Branching and Switching](#-branching-and-switching)
    - [🏷️ Tagging Releases](#️-tagging-releases)
    - [🚫 Ignoring Files](#-ignoring-files)
      - [Sample `.gitignore`](#sample-gitignore)
  - [3.4 Summarize common infrastructure as code technologies](#34-summarize-common-infrastructure-as-code-technologies)
    - [📄 File Formats](#-file-formats)
    - [🔧 IaC Utilities](#-iac-utilities)
    - [🚀 CI/CD Integration](#-cicd-integration)
      - [🔄 Common Use Cases](#-common-use-cases)
    - [🧠 Advanced Git Topics](#-advanced-git-topics)
      - [Merge vs. Rebase:](#merge-vs-rebase)
  - [3.5 Summarize container, cloud, and orchestration concepts](#35-summarize-container-cloud-and-orchestration-concepts)
    - [⚙️ Kubernetes Overview](#️-kubernetes-overview)
      - [✅ Benefits](#-benefits)
      - [🧩 Key Components](#-key-components)
    - [🖥️ Single-Node \& Multicontainer Use Cases](#️-single-node--multicontainer-use-cases)
    - [💾 Container Persistent Storage](#-container-persistent-storage)
      - [Docker Example:](#docker-example)
    - [🌐 Container Networking](#-container-networking)
      - [Example: Exposing a Web App](#example-exposing-a-web-app)
    - [🔄 Service Mesh](#-service-mesh)
      - [✨ Key Features](#-key-features)
    - [🚀 Bootstrapping with Cloud-Init](#-bootstrapping-with-cloud-init)
      - [🧰 Common Tasks](#-common-tasks)
      - [Example:](#example-2)
    - [📥 Container Registries](#-container-registries)
      - [🗃️ Types of Registries](#️-types-of-registries)
      - [🔁 Image Lifecycle Workflow](#-image-lifecycle-workflow)
      - [🔐 Securing Registries](#-securing-registries)
        - [🔒 Security Practices](#-security-practices)
        - [🔐 Example: Authenticating and Pushing Securely](#-example-authenticating-and-pushing-securely)
- [4.0 Troubleshooting](#40-troubleshooting)
  - [4.1 Given a scenario, analyze and troubleshoot storage issues](#41-given-a-scenario-analyze-and-troubleshoot-storage-issues)
    - [🐢 High Latency](#-high-latency)
      - [Suggested Actions](#suggested-actions)
    - [📉 Low Throughput](#-low-throughput)
      - [Suggested Actions](#suggested-actions-1)
    - [🧮 IOPS Issues](#-iops-issues)
      - [Suggested Actions](#suggested-actions-2)
    - [💾 Capacity Issues](#-capacity-issues)
    - [📁 Filesystem Issues](#-filesystem-issues)
    - [⏱️ I/O Scheduler](#️-io-scheduler)
    - [🔧 Device-Level Issues](#-device-level-issues)
      - [📘 Common Devices and Diagnostics](#-common-devices-and-diagnostics)
      - [🔍 Sample Troubleshooting](#-sample-troubleshooting)
    - [🧱 Mount Option Problems](#-mount-option-problems)
      - [🚩 Common Mount Options and Their Impacts](#-common-mount-options-and-their-impacts)
      - [🔍 Diagnosing Mount Problems](#-diagnosing-mount-problems)
  - [4.2 Given a scenario, analyze and troubleshoot network resource issues](#42-given-a-scenario-analyze-and-troubleshoot-network-resource-issues)
    - [⚙️ Network Configuration Issues](#️-network-configuration-issues)
      - [Subnet Problems](#subnet-problems)
      - [Routing Issues](#routing-issues)
      - [🔍 Example:](#-example)
    - [🔥 Firewall Issues](#-firewall-issues)
      - [🔍 Diagnosis and Tools](#-diagnosis-and-tools)
      - [🧪 Troubleshooting Steps](#-troubleshooting-steps)
    - [🖧 Interface Errors](#-interface-errors)
      - [➤ Dropped Packets](#-dropped-packets)
      - [➤ Collisions](#-collisions)
      - [➤ Link Status](#-link-status)
      - [📋 Common Interface Issues](#-common-interface-issues)
      - [🔍 Diagnostic Examples](#-diagnostic-examples)
    - [📉 Bandwidth Limitations \& High Latency](#-bandwidth-limitations--high-latency)
      - [➤ High Latency](#-high-latency-1)
      - [⚠️ Common Causes](#️-common-causes)
      - [🧪 Diagnostic Tools and Usage](#-diagnostic-tools-and-usage)
    - [🌐 Name Resolution Issues](#-name-resolution-issues)
      - [➤ DNS](#-dns)
    - [🧪 Testing Remote Systems](#-testing-remote-systems)
      - [➤ Nmap](#-nmap)
      - [➤ openssl s\_client](#-openssl-s_client)
  - [4.3 Given a scenario, analyze and troubleshoot central processing unit (CPU) and memory issues](#43-given-a-scenario-analyze-and-troubleshoot-central-processing-unit-cpu-and-memory-issues)
    - [🧵 Process-Related Issues](#-process-related-issues)
      - [➤ Runaway Processes](#-runaway-processes)
      - [➤ Zombie Processes](#-zombie-processes)
    - [📈 CPU Load \& Utilization](#-cpu-load--utilization)
      - [➤ High CPU Utilization](#-high-cpu-utilization)
      - [➤ High Load Average](#-high-load-average)
      - [➤ High Run Queues](#-high-run-queues)
    - [⏱ CPU Time Metrics](#-cpu-time-metrics)
    - [🎚 CPU Priorities](#-cpu-priorities)
      - [➤ nice / renice](#-nice--renice)
    - [🧠 Memory Management](#-memory-management)
      - [➤ Memory Exhaustion](#-memory-exhaustion)
      - [➤ Out Of Memory (OOM)](#-out-of-memory-oom)
      - [➤ Memory Leaks](#-memory-leaks)
    - [🔄 Swapping](#-swapping)
    - [🔧 Hardware Inspection](#-hardware-inspection)
  - [4.4 Given a scenario, analyze and troubleshoot user access and file permissions](#44-given-a-scenario-analyze-and-troubleshoot-user-access-and-file-permissions)
    - [🔑 User Login Issues](#-user-login-issues)
    - [🗂️ User File Access Issues](#️-user-file-access-issues)
      - [➤ Group](#-group)
      - [➤ Context (SELinux/AppArmor)](#-context-selinuxapparmor)
      - [➤ Permission](#-permission)
      - [➤ ACL (Access Control Lists)](#-acl-access-control-lists)
      - [➤ Attribute](#-attribute)
      - [➤ Policy vs. Non-Policy](#-policy-vs-non-policy)
    - [🔐 Password Issues](#-password-issues)
    - [🧰 Privilege Elevation](#-privilege-elevation)
    - [📊 Quota Issues](#-quota-issues)
# CompTIA Linux+ Exam XK0-005
# 1.0 System Management
## 1.1 Summarize Linux fundamentals
### 📁 Filesystem Hierarchy Standard (FHS)
Linux organizes files by function in specific directories:
- `/boot` – Bootloader files (e.g. GRUB, kernels)
- `/proc` – Virtual filesystem exposing kernel & process info
- `/sys` – Interface to kernel devices and hardware
- `/var` – Variable data like logs and mail
- `/usr` – User utilities and applications
- `/lib` – Shared system libraries
- `/dev` – Device files (block & character devices)
- `/etc` – System configuration files
- `/opt` – Optional third-party software
- `/bin`, `/sbin` – Essential binaries (user & root)
- `/home` – User directories
- `/media`, `/mnt` – Mount points for external storage
- `/root` – Root user’s home
- `/tmp` – Temporary files
### 🧃 Basic Boot Process
Steps that bring Linux to life:
- **BIOS/UEFI** – Firmware initialization and boot device selection
- **Bootloader** – GRUB2 loads kernel & initrd
- **Kernel** – vmlinuz is the compressed Linux kernel
- **Initrd/initramfs** – Temporary root filesystem for early boot
#### 🔧 Boot Commands
- `mkinitrd` / `dracut` – Create initial RAM disk
- `grub2-install` – Install GRUB2
- `grub2-mkconfig` / `grub2-update` – Generate/update GRUB config
#### 🌀 Boot Sources
- **PXE** – Network boot via BIOS/UEFI
- **USB** – Bootable flash drives
- **ISO** – Disk image boot via virtual media
#### 💥 Kernel Panic
System crash due to unrecoverable kernel error—usually visible during boot or hardware issues.
### ⚙️ /dev Device Types
- **Block devices** – Data in blocks (e.g., hard drives)
- **Character devices** – Data stream (e.g., keyboards)
- **Special**:
  - `/dev/null` – Bit bucket (discard output)
  - `/dev/zero` – Infinite zeros
  - `/dev/urandom` – Pseudo-random data
### 🔨 Package Compilation (from Source)
Typical 3-step build:
```bash
./configure
make
make install
```
## 1.2 Given a scenario, manage files and directories
This section outlines key Linux tools and commands for working with files and directories across various scenarios.
### ✏️ File Editing
Efficient tools to inspect or manipulate file contents:
- `sed` – Stream editor; perform substitutions and transformations:
  ```shell
  sed 's/old/new/g' file.txt
  ```
- `awk` – Pattern scanning and processing (great for structured text):
  ```shell
  awk – Pattern scanning and processing (great for structured text):
  ```
- `printf` – Format and output text:
  ```shell
  printf "Name: %s\n" "$USER"
  ```
- `nano` – Simple terminal-based text editor.
- `vi / vim` – Powerful modal editor with extensive navigation & editing capabilities.
### 📦 File Compression, Archiving, and Backup
Tools to reduce size and create archives:
- `gzip, bzip2, xz, zip` – Compress files:
  ```shell
  gzip file.txt
  ```
- `tar` – Archive files:
  ```shell
  tar -cvf archive.tar folder/
  ``
- `cpio` – Archive and extract, often used with `find`.
- `dd` – Disk clone or backup tool:
  ```shell
  dd if=/dev/sda of=/backup.img bs=4M
  ```
### 🗃️ File Metadata
View file type and attributes:
- `stat` – Shows detailed file info (size, access time, etc.)
- `file` – Detects file type based on content.
### 🔗 Soft and Hard Links
- Soft link (symbolic):
  ```shell
  ln -s original.txt shortcut.txt
  ```
- Hard link:
  ```shell
  ln original.txt link.txt
  ```
### 🌐 Copying Files Between Systems
Used for remote syncing and file transfer:
- `rsync` – Efficient sync across systems or drives:
  ```shell
  rsync -avz src/ user@host:/dest/
  ```
- `scp` – Secure copy over SSH:
  ```shell
  scp file.txt user@host:/path/
  ```
- `nc` (netcat) – Raw network data transfer (advanced use cases).
### 🧱 File & Directory Operations
General navigation and management:
- `mv` – Move or rename files
- `cp` – Copy files
- `mkdir / rmdir` – Create or remove directories
- `ls` – List directory contents
- `pwd` – Show current working directory
- `rm` – Remove files or directories
- `cd` – Change directory
- `.` – Current directory
- `..` – Parent directory
- `~` – Home directory
- `tree` – Graphical directory structure
- `cat` – Display file contents
- `touch` – Create empty files or update timestamps
## 1.3 Given a scenario, configure and manage storage using the appropriate tools
Efficient storage setup in Linux often requires understanding disks, filesystems, logical volumes, and network storage.
### 🔧 Disk Partitioning
Tools to define disk layout:
- `fdisk` – Manage MBR partitions on block devices.
- `parted` – Flexible tool for GPT and MBR partitioning:
  ```bash
  parted /dev/sda mkpart primary ext4 1MiB 1000MiB
  ```
- `partprobe` – Inform kernel of partition table changes.
### 📂 Mounting Local and Remote Devices
Enabling access to storage volumes:
- `mount` – Mount a device or filesystem:
  ```shell
  mount /dev/sdb1 /mnt/data
  ```
- `systemd.mount` – Auto-mount via systemd unit file.
- `/etc/fstab` – Persistent mount definitions at boot.
- External Devices – USBs, external drives auto-detected at /media or via manual mount.
- LUKS – Encrypt disk partitions using:
  ```shell
  cryptsetup luksFormat /dev/sdX
  ```
### 🧮 Filesystem Management
Native filesystem tools:
- XFS – Use `xfsprogs` (e.g. `xfs_repair`, `xfs_info`)
- Ext4 – Use `e2fsprogs` (e.g. `e2fsck`, `resize2fs`)
- Btrfs – Use `btrfs` CLI tool for snapshots, compression, and balancing.
### 📊 Monitoring Storage and Usage
Disk space and file size tracking:
- `df -h` – View filesystem disk usage (human-readable).
- `du -sh folder/` – Show size of directory recursively.
### 🧱 Logical Volume Manager (LVM)
Flexible disk abstraction and resizing:
- Physical Volumes:
  - `pvcreate` – Initialize a disk for LVM.
  - `pvs` – List physical volumes.
- Volume Groups:
  - `vgcreate` – Create a group of physical volumes.
  - `vgextend` – Add physical volume to a group.
  - `vgs` – Display volume groups.
- Logical Volumes:
  - `lvcreate` – Make a logical volume:
    ```shell
    lvcreate -L 10G -n mylv myvg
    ```
  - `lvresize / lvchange` – Modify volume size or attributes.
  - `lvs` – List logical volumes.
### 🔁 Inspecting RAID
For software-based RAID arrays:
- `mdadm` – Configure and monitor RAID devices:
  ```shell
  mdadm --detail /dev/md0
  ```
- `/proc/mdstat` – Realtime RAID status overview.
### 🌐 SAN/NAS and Network Filesystems
Enterprise-level or remote storage:
- `multipathd` – Support for multipath I/O (used in SANs).
- NFS – Mount Unix-style shared directories:
  ```shell
  mount -t nfs server:/share /mnt
  ```
- SMB/CIFS – Connect to Windows shares:
  ```shell
  mount -t cifs -o username=user //server/share /mnt
  ```
### 🔍 Storage Hardware Inspection
Tools to probe attached devices:
- `lsscsi` – List SCSI devices.
- `lsblk` – Tree view of block devices.
- `blkid` – Identify block device UUIDs and filesystem types.
- `fcstat` – Fibre Channel status tool for SAN diagnostics.
## 1.4 Given a scenario, configure and use the appropriate processes and services
This section covers managing system processes and services using built-in Linux utilities and scheduling tools.
### 🛎️ System Services with `systemctl`
Manage services on systems using `systemd`:
- `systemctl stop service` – Stop a service
- `systemctl start service` – Start a service
- `systemctl restart service` – Restart a service
- `systemctl status service` – View service status
- `systemctl enable service` – Enable at boot
- `systemctl disable service` – Disable from boot
- `systemctl mask service` – Prevent service from starting at all

Example:
```bash
systemctl start nginx
systemctl enable sshd
```
### ⏰ Scheduling Services
Automate tasks with time-based execution:
- `cron` – Daemon for recurring tasks (minute/hour/day/month/week)
- `crontab` – Per-user cron schedule editor:
  ```shell
  crontab -e  # Edit your schedule
  ```
- `at` – Schedule one-time tasks:
  ```shell
  echo "reboot" | at now + 1 hour
  ```
### 🧠 Process Management
Control and inspect running processes.
#### 💥 Kill Signals
Signals sent to running processes:
- `SIGTERM` – Graceful termination (default)
- `SIGKILL` – Forceful kill; process can't ignore
- `SIGHUP` – Hangup signal; often used to reload configuration
```shell
kill -SIGTERM <PID>
kill -9 <PID>         # Sends SIGKILL
```
#### 📋 Listing Processes and Open Files
- `ps aux` – Full list of running processes
- `top / htop` – Dynamic live monitoring (htop is more interactive)
- `lsof` – List open files and associated processes
#### 📌 Setting Process Priorities
Control how much CPU a process gets:
- `nice` – Start a process with a priority:
  ```shell
  nice -n 10 command
  ```
- `renice` – Change priority of an existing process:
  ```shell
  renice -n -5 -p <PID>
  ```
#### 🌡️ Process States
Linux process lifecycle stages:
- Running – Actively executing
- Sleeping – Waiting for I/O or event
- Stopped – Halted by signal
- Zombie – Completed, waiting for parent to acknowledge exit
#### 🎮 Job Control (Terminal Jobs)
Manage background and foreground tasks in the shell:
- `Ctrl+Z` – Suspend process
- `bg` – Resume in background
- `fg` – Bring job to foreground
- `jobs` – List background jobs
- `Ctrl+C` – Kill foreground job
- `Ctrl+D` – End input (often logs out or closes terminal)
#### 🔍 Searching & Terminating Processes
- `pgrep` – Find processes by name:
  ```shell
  pgrep apache2
  ```
- `pkill` – Kill processes by name:
  ```shell
  pkill -9 firefox
  ```
- `pidof` – Get PID of a running program:
  ```shell
  pidof sshd
  ```
## 1.5 Given a scenario, use the appropriate networking tools or configuration files
This guide outlines how to configure and manage networking using the most relevant Linux tools and files.
### 🔌 Interface Management
Configure IP addresses, view interfaces, and routes:
#### 🧰 iproute2 Tools
- `ip` – Manage interfaces, addresses, routes:
  ```bash
  ip addr show
  ip route add default via 192.168.1.1
  ```
- `ss` – View socket connections and listening ports:
  ```shell
  ss -tunlp
  ```
#### 📡 NetworkManager
- `nmcli` – Manage connections interactively or via script:
  ```shell
  nmcli dev show
  nmcli con up eth0
  ```
#### 🔧 Legacy Net-Tools
- `ifconfig` – View or configure interfaces (older systems)
- `ifcfg-*` – Interface configuration files for Red Hat systems
- `hostname` – Set or view system hostname
- `arp` – View or manipulate ARP table
- `route` – View or modify routing table
#### 🗂️ Configuration Files
- `/etc/sysconfig/network-scripts/` – Interface and routing configs (used by `ifcfg-*`)
### 📛 Name Resolution
Translate hostnames into IP addresses:
- `/etc/nsswitch.conf` – Configures name service lookup order.
- `/etc/resolv.conf` – DNS servers defined here.
- `hostnamectl` – Set persistent hostname.
- `resolvectl` – Query and manage DNS using systemd-resolved.
#### 🔍 DNS Tools (Bind-utils)
- `dig` – Detailed DNS queries:
  ```bash
  dig www.example.com
  ```
- `nslookup` – Simple DNS lookup:
  ```shell
  nslookup example.com
  ```
- `host` – Hostname-to-IP resolution:
  ```shell
  host example.com
  ```
#### 🌎 WHOIS
- `whois` – Fetch domain registration info:
  ```shell
  whois example.com
  ```
### 📊 Network Monitoring
Capture packets, analyze traffic, and trace connectivity:
- `tcpdump` – Lightweight packet sniffer:
  ```bash
  tcpdump -i eth0 port 80
  ```
- `wireshark / tshark` – Detailed protocol analysis (GUI and CLI).
- `netstat` – Show network connections and routing info (deprecated in favor of `ss`)
- `traceroute` – Display path to a host across the network:
  ```shell
  traceroute example.com
  ```
- `ping` – Test reachability and latency:
  ```shell
  ping -c 4 example.com
  ```
- `mtr` – Real-time traceroute and ping hybrid:
  ```shell
  mtr example.com
  ```
### 📡 Remote Networking Tools
Transfer files, retrieve data, and connect to remote hosts:
- `ssh` – Secure shell remote login:
  ```shell
  ssh user@host
  ```
- `curl` – Transfer data using protocols (HTTP, FTP):
  ```shell
  curl https://example.com
  ```
- `wget` – Download files from web sources:
  ```shell
  wget https://example.com/file.zip
  ```
- `nc` (netcat) – Versatile TCP/UDP utility (debugging or transfers):
  ```shell
  nc -l -p 1234 > received_file
  ```
- `rsync` – Remote synchronization with compression and delta support:
  ```shell
  rsync -avz /data user@host:/backup
  ```
- `scp` – Secure copy via SSH:
  ```shell
  scp file.txt user@host:/target/path/
  ```
- `sftp` – Interactive secure file transfer session:
  ```shell
  sftp user@host
  ```
## 1.6 Given a scenario, build and install software
This section outlines essential tools and methods to manage software—from package managers to sandboxed apps and system updates.
### 📦 Package Management
Each Linux distribution uses a different package manager for installing and updating software:
| Manager | Distro(s) | Commands |
|--------|------------|----------|
| `dnf`  | Fedora, RHEL, CentOS (new) | `dnf install <package>` |
| `yum`  | RHEL, CentOS (legacy) | `yum install <package>` |
| `apt`  | Debian, Ubuntu | `apt install <package>` |
| `rpm`  | RHEL-based | `rpm -ivh <package>.rpm` |
| `dpkg` | Debian-based | `dpkg -i <package>.deb` |
| `ZYpp` | openSUSE | `zypper install <package>` |

For example, to install nginx on Ubuntu:
```bash
sudo apt update
sudo apt install nginx
```
### 🧪 Sandboxed Applications
Portable or containerized app formats with isolated dependencies:
- `snapd` – Snap packages (auto-update & confinement):
  ```shell
  sudo snap install <app>
  ```
- `Flatpak` – Decentralized packaging with permission control:
  ```shell
  flatpak install flathub org.gimp.GIMP
  ```
- AppImage – Executable format; no installation:
  ```shell
  chmod +x <AppImage>.AppImage
  ./<AppImage>.AppImage
  ```
### 🔄 System Updates
Keep your system secure and up-to-date:
#### 🔧 Kernel Updates
Most distros update the kernel via package managers:
```shell
sudo dnf update kernel
sudo apt upgrade linux-image
```
Reboot after updating to activate the new kernel.
#### 📥 Package Updates
Update all installed packages:
```shell
sudo apt update && sudo apt upgrade
sudo dnf upgrade
sudo zypper update
```
## 1.7 Given a scenario, manage software configurations
This guide walks through updating system settings, managing configuration files, kernel parameters, and common services.
### 🔧 Updating Configuration Files
#### 🔄 Procedures
After editing a config file, apply changes using:
- **Restart the service** – Full stop/start cycle:
  ```bash
  systemctl restart <service>
  ```
- **Reload the service** – Reloads config without full restart (if supported):
  ```shell
  systemctl reload <service>
  ```
#### 🗂️ RPM-based Config File Management
When updating packages:
- `.rpmnew` – New version of config file delivered; original untouched
- `.rpmsave` – Original config saved before update replaces it
Check and compare these files manually:
```shell
diff /etc/example.conf /etc/example.conf.rpmnew
```
#### 📁 Repository Configuration Files
Manage repository sources and behavior:
- `/etc/apt.conf` – Global APT settings (Ubuntu/Debian)
- `/etc/apt/sources.list.d/` – Repo definitions
- `/etc/yum.conf` – YUM configuration
- `/etc/dnf/dnf.conf` – DNF settings
- `/etc/yum.repos.d/` – Repo definitions in .repo files
### 🧪 Configure Kernel Options
#### ⚙️ Kernel Parameters
Used for tuning system behavior:
- View parameters:
```shell
sysctl -a
```
- Set a parameter:
```shell
sudo sysctl net.ipv4.ip_forward=1
```
- Make permanent in `/etc/sysctl.conf`
#### 🧩 Kernel Modules
Manage loadable kernel extensions:
| Command   | Description                           |
|-----------|---------------------------------------|
| `lsmod`   | List loaded modules                   |
| `modinfo` | Show module details                   |
| `insmod`  | Insert module manually                |
| `rmmod`   | Remove a module                       |
| `modprobe`| Load module with dependencies         |
| `imsmod`  | Deprecated variant of `insmod`        |

Example:
```shell
modprobe usb-storage
```
### 🛠️ Configure Common System Services
| Service | Configuration Path or Tool                              |
|---------|---------------------------------------------------------|
| SSH     | `/etc/ssh/sshd_config`                                  |
| NTP     | `/etc/ntp.conf` or via `ntpd`                           |
| chrony  | `/etc/chrony.conf` (modern NTP alternative)             |
| Syslog  | `/etc/rsyslog.conf` or journald settings                |

After updates:
```shell
systemctl restart sshd
systemctl reload rsyslog
```
### 🌍 Localization Tools
Set system locale, time zone, and language preferences:
- `timedatectl` – Set time, timezone, NTP:
```shell
timedatectl set-timezone America/Montreal
```
- `localectl` – Configure language and keyboard layout:
```shell
localectl set-locale LANG=en_CA.UTF-8
```
# 2.0 Security
## 2.1 Summarize the purpose and use of security best practices in a Linux environment
In a Linux environment, security involves layered techniques to protect system integrity, confidentiality, and availability. Below is a structured overview.
### 🛡️ Public Key Infrastructure (PKI) Certificates
PKI helps secure data exchange using cryptographic keys and certificates:
| Concept                | Purpose                                              |
|------------------------|------------------------------------------------------|
| **Public key**         | Shared openly; encrypts data and verifies signatures |
| **Private key**        | Kept secret; decrypts data and signs messages        |
| **Self-signed cert**   | Issued without a CA; used in testing/dev environments|
| **Digital signature**  | Verifies authenticity of sender using private key    |
| **Wildcard certificate**| Covers all subdomains (e.g., `*.example.com`)       |
| **Hashing**            | Ensures data integrity (e.g., SHA256)                |
| **Certificate authority** | Trusted entity that issues digital certificates   |
### 🔒 Certificate Use Cases
Certificates help secure communication and verify identity:
- **SSL/TLS** – Encrypted communication via HTTPS or secure email.
- **Authentication** – Verifies server identity and prevents impersonation.
- **Encryption** – Ensures sensitive data (e.g., login credentials) stays private.
### 👤 Authentication Technologies
Secure access control and identity validation:
| Method                         | Description                                    |
|--------------------------------|------------------------------------------------|
| **Tokens**                     | Time-based or hardware-generated access codes  |
| **Multifactor Authentication (MFA)** | Combines password + token, fingerprint, etc. |
| **PAM**                        | Modular system for flexible authentication     |
| **SSSD**                       | Provides access to remote identity/data sources|
| **LDAP**                       | Centralized directory for users & permissions  |
| **Single Sign-On (SSO)**       | Login once, access multiple systems/services   |
### 🧱 Linux Hardening
Strengthen system configuration to reduce vulnerabilities:
#### 🔍 Security Measures
- **Security scanning** – Detect known vulnerabilities (e.g., with `lynis`, `clamav`, or `OpenSCAP`)
- **Secure boot** – Ensure only trusted software loads at boot
- **UEFI** – Modern firmware with Secure Boot support
#### ⚙️ System Configuration
- **System logging** – Configure `rsyslog` or `journald` to monitor activity
- **Default umask** – Sets file permission defaults to prevent overexposure
- **Disable insecure services** – Remove legacy or unused daemons (e.g., telnet)
- **Enforce password strength** – Use `pam_pwquality` or `passwdqc`
- **Remove unused packages** – Reduce attack surface and dependencies
- **Tune kernel parameters** – Via `sysctl.conf` for performance and security
- **Secure service accounts** – Restrict permissions and access
- **Host firewall** – Use `iptables`, `firewalld`, or `nftables` to manage traffic
## 2.2 Given a scenario, implement identity management
Managing user and group identities ensures secure, organized access control in multi-user systems. Here's a breakdown of key tools, files, and practices.
### 👤 Account Creation and Deletion
Create or remove user and group identities:
| Command      | Description                              |
|--------------|------------------------------------------|
| `useradd`    | Add a new user                           |
| `groupadd`   | Create a new group                       |
| `userdel`    | Remove a user and their account          |
| `groupdel`   | Remove a group                           |
| `usermod`    | Modify a user (e.g. group, shell)        |
| `groupmod`   | Modify group info                        |
| `id`         | Show user ID, group ID, and group info   |
| `who`        | List logged-in users                     |
| `w`          | Show who’s logged in and what they’re doing

Example:
```bash
useradd -m -s /bin/bash arthur
passwd arthur
```
### 🐚 Default Shell and Skeleton Files
Set user environment defaults:
- **Default shell** is defined using `-s` with `useradd` or via `/etc/default/useradd`.
- Skeleton files are copied to new users from:
  - `/etc/skel/` – Template files placed into a new user's home directory.
  - `.bash_profile`, `.bashrc` – Shell-specific initialization and environment settings.
### 🗄️ Configuration Files
Linux stores identity details in structured text files:
| File              | Purpose                                         |
|-------------------|-------------------------------------------------|
| `/etc/passwd`     | Username, UID, shell, home directory            |
| `/etc/group`      | Group names and memberships                     |
| `/etc/shadow`     | Encrypted user passwords and aging info         |
| `/etc/profile`    | Global environment variables and shell settings |
| `/etc/skel/`      | Default content copied to new home directories  |
### 🔐 Account Management Tools
Control passwords, expiration, and failed login behavior:
- `passwd` – Set or change user password.
- `chage` – Configure password aging policies:
  ```bash
  chage -E 2025-12-31 arthur
  ```
- `pam_tally2` – Monitor failed login attempts (Debian/Ubuntu).
- `faillock` – Lock account after consecutive failed attempts (RHEL/Fedora).
- `/etc/login.defs` – Set global defaults (UID ranges, aging policies).
## 2.3 Given a scenario, implement and configure firewalls
Firewalls are vital for securing your system by controlling incoming and outgoing traffic based on defined rules. Below is a structured overview of tools and concepts to guide firewall implementation.
### 🎯 Firewall Use Cases
| Task                           | Command Example                                     |
|--------------------------------|-----------------------------------------------------|
| **Open a port**               | `firewall-cmd --add-port=443/tcp --permanent`      |
| **Close a port**              | `iptables -D INPUT -p tcp --dport 22 -j ACCEPT`     |
| **Check firewall config**     | `firewall-cmd --list-all` or `iptables -L -n`       |
| **Enable IP forwarding**      | `sysctl -w net.ipv4.ip_forward=1`                   |
| **Disable IP forwarding**     | `sysctl -w net.ipv4.ip_forward=0`                   |

To persist IP forwarding changes, update `/etc/sysctl.conf`:
```bash
net.ipv4.ip_forward = 1
```
### 🛠️ Common Firewall Technologies
Linux offers several powerful tools for managing network traffic:
#### 🔹 firewalld
- Dynamic and zone-based firewall manager.
- Supports runtime and permanent configuration.
- Common commands:
```bash
firewall-cmd --get-active-zones
firewall-cmd --add-service=http --permanent
firewall-cmd --reload
```
#### 🔹 iptables
- Legacy tool for packet filtering.
- Rule-based syntax and highly scriptable.
Example usage:
```shell
iptables -A INPUT -p tcp --dport 80 -j ACCEPT
iptables -L -n
```
#### 🔹 nftables
- Modern replacement for iptables.
- Unified framework for IPv4/IPv6 and better syntax.
Example usage:
```shell
nft list ruleset
nft add rule inet filter input tcp dport 22 accept
```
#### 🔹 UFW (Uncomplicated Firewall)
- Simpler interface for iptables (common on Ubuntu).
- Ideal for beginner and quick setups.
Commands:
```shell
ufw allow 22/tcp
ufw enable
ufw status
```
#### 🔐 Key Firewall Features
| Feature   | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| **Zones**     | Isolated contexts for defining access levels (`firewalld`)                  |
| **Services**  | Grouped definitions of ports and protocols (e.g., SSH, HTTP)                |
| **Stateful**  | Tracks and remembers connection states for intelligent filtering            |
| **Stateless** | Treats each packet independently; rules applied without context             |
## 2.4 Given a scenario, configure and execute remote connectivity for system management
SSH (Secure Shell) is the foundation of secure remote administration in Linux. It allows encrypted access, tunneling, and command execution across systems. Here's a practical breakdown.
### 🔐 SSH Configuration Files
| File                        | Purpose                                              |
|-----------------------------|------------------------------------------------------|
| `/etc/ssh/sshd_config`      | Server-side SSH daemon settings                     |
| `/etc/ssh/ssh_config`       | Client-side default settings                        |
| `~/.ssh/known_hosts`        | Tracks trusted remote hosts                         |
| `~/.ssh/authorized_keys`    | Lists public keys allowed for key-based login       |
| `~/.ssh/config`             | User-specific client settings (hosts, keys, ports)  |

Example `~/.ssh/config` entry:
```ini
Host webserver
    HostName 192.168.1.10
    User arthur
    IdentityFile ~/.ssh/id_rsa
```
### 🔑 SSH Commands
SSH utilities streamline authentication, secure key handling, and remote access:
| Command        | Purpose                                               |
|----------------|--------------------------------------------------------|
| `ssh-keygen`   | Generate SSH key pair (e.g., RSA, ED25519)             |
| `ssh-copy-id`  | Copy your public key to a remote server for key-based login |
| `ssh-add`      | Add key to SSH agent for automatic authentication      |
#### Example Workflow:
```bash
# Generate a key pair
ssh-keygen -t ed25519

# Transfer your public key to another system
ssh-copy-id user@remotehost

# Use the key to connect
ssh user@remotehost
```
### 🔀 SSH Tunneling Techniques
Securely forward traffic or enable remote GUI sessions:
| Method              | Description                                        | Example Command                                  |
|---------------------|----------------------------------------------------|--------------------------------------------------|
| **X11 Forwarding**  | Run graphical applications remotely                | `ssh -X user@host`                               |
| **Port Forwarding** | Redirect a local port to a remote service          | `ssh -L 8080:localhost:80 user@host`             |
| **Dynamic Forwarding** | Create a SOCKS proxy for multiple destinations | `ssh -D 1080 user@host`                          |
#### 👥 Executing Commands as Another User
Switch users or elevate privileges securely.
#### 🔧 Configuration Files
- `/etc/sudoers` – Central file defining sudo permissions
- **PolicyKit Rules** – Used by `pkexec` for GUI/service access controls
#### 🛠️ Common Privilege-Elevation Commands
| Command   | Purpose                                                 |
|-----------|----------------------------------------------------------|
| `sudo`    | Run commands with superuser privileges                  |
| `visudo`  | Safely edit `/etc/sudoers` with syntax validation       |
| `su -`    | Start a login shell as another user (commonly root)     |
| `pkexec`  | Prompt for elevated access to run graphical tools       |
#### Example Usage:
```bash
# Update packages with root privileges
sudo apt update

# Switch to root account
su -

# Launch GUI text editor as root
pkexec gedit /etc/ssh/sshd_config
```
## 2.5 Given a scenario, apply the appropriate access controls
Access control mechanisms ensure that users, applications, and processes only interact with files and resources they’re authorized to. Here’s how to configure them effectively.
### 📁 File Permissions
Traditional Unix permissions involve:
- **Owner**, **Group**, and **Other**
- `r` (read), `w` (write), `x` (execute)
#### 🔧 Extended Attributes
| Feature          | Description                                                         |
|------------------|---------------------------------------------------------------------|
| **ACL (Access Control List)** | Fine-grained permissions beyond owner/group: `getfacl`, `setfacl` |
| **SUID (Set User ID)**        | Executed file runs with owner's privileges             |
| **SGID (Set Group ID)**       | Directory: new files inherit group. File: runs with group privileges |
| **Sticky Bit**                | Prevents file deletion except by file owner (e.g. `/tmp`) |
#### Example:
```bash
chmod 4755 /usr/bin/example   # Sets SUID
chmod 2770 /data              # SGID for group inheritance
chmod +t /shared              # Sticky bit
```
### 🛡️ SELinux (Security-Enhanced Linux)
SELinux provides Mandatory Access Control (MAC) for enhanced system protection. It enforces policies using file and process labels, managing access based on roles and types.
#### 📦 Context & Label Management
| Tool/Command    | Purpose                                             |
|-----------------|-----------------------------------------------------|
| `ls -Z`         | View SELinux context labels                        |
| `chcon`         | Change security context of a file temporarily      |
| `restorecon`    | Restore default SELinux context from policy        |
| `semanage`      | Persistent context and port modifications          |

- **Autorelabel** – Forces a full system relabel at reboot:
```bash
touch /.autorelabel && reboot
```
#### 📋 SELinux States
SELinux can operate in three modes, each affecting how policies are enforced:
| Mode         | Behavior                                               |
|--------------|--------------------------------------------------------|
| **Enforcing**  | Actively blocks unauthorized access according to SELinux policy |
| **Permissive** | Logs policy violations without enforcing restrictions |
| **Disabled**   | Completely disables SELinux enforcement and logging   |

Check current SELinux mode:
```bash
getenforce
```
Switch mode temporarily (until reboot):
```shell
setenforce 0   # Permissive
setenforce 1   # Enforcing
```
#### 🔁 System Booleans
SELinux booleans allow you to toggle specific access controls without rewriting policy definitions.
| Command                        | Function                                                   |
|--------------------------------|------------------------------------------------------------|
| `getsebool <boolean>`          | View the current value of a boolean setting               |
| `setsebool <boolean> on|off`   | Set a boolean temporarily until next reboot               |
| `setsebool -P <boolean> on|off`| Apply the change persistently across reboots              |
##### Example:
```bash
getsebool httpd_can_network_connect
setsebool -P httpd_can_network_connect on
```
#### 🔐 Policy Types
SELinux supports multiple policy types tailored to different security needs:
| Policy Type     | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| **Targeted**     | Applies policies only to selected critical services (default in most systems) |
| **Minimum**      | Applies minimal restrictions; useful for testing or lightweight configurations |

These policies define how rigorously SELinux enforces access controls across the system. “Targeted” provides a balance between usability and security, while “Minimum” is helpful for environments where stricter enforcement might interfere with essential services.
# 3.0 3.0 Scripting, Containers, and Automation
## 3.1 Given a scenario, create simple shell scripts to automate common tasks
Shell scripts help automate repetitive tasks like backups, file processing, and system maintenance. Below is an organized reference of key elements used in basic scripting scenarios.
### 🔁 Loops
| Type     | Purpose                                      | Example                     |
|----------|----------------------------------------------|-----------------------------|
| `while`  | Loop until condition becomes false           | `while [ "$count" -lt 5 ]; do ...; done` |
| `for`    | Iterate over a list                          | `for file in *.log; do ...; done` |
| `until`  | Loop until condition becomes true            | `until ping -c1 host; do ...; done` |
### 🔀 Conditionals
| Structure      | Example                                               |
|----------------|-------------------------------------------------------|
| `if`           | `if [ "$var" -eq 1 ]; then echo "Yes"; fi`           |
| `case`         | `case "$option" in 1) echo "One";; 2) echo "Two";; esac` |
### 🧪 Parameter Expansion & Patterns
| Feature            | Description                                 |
|--------------------|---------------------------------------------|
| **Globbing**       | Pattern matching: `*.txt`, `data??.csv`     |
| **Brace Expansions** | Generate strings: `{01..05}`, `{a,b,c}`    |
### 🔢 Comparisons
| Type       | Sample Expression                              |
|------------|-------------------------------------------------|
| Arithmetic | `(( x > y ))`                                   |
| String     | `[ "$a" = "$b" ]`                               |
| Boolean    | `[[ $x -gt 10 && $y -lt 5 ]]`                   |
### 📦 Variables & Input
| Feature      | Example                         |
|--------------|---------------------------------|
| Set variable | `name="Arthur"`                 |
| Read input   | `read username`                 |
| Expand       | `echo "User: $username"`        |
| Source       | `source ~/.bash_profile`        |
### 🔄 Search and Replace
| Tool   | Usage                                      |
|--------|---------------------------------------------|
| `sed`  | `sed 's/foo/bar/g' file.txt`               |
| `awk`  | `awk '{print $1}' file.txt`                |
| `grep` | `grep "pattern" file.txt`                  |
| `find` | `find /path -name "*.log"`                 |
| `xargs`| `find . -name '*.log' | xargs rm`          |
### 📊 Standard Stream Redirection
| Operator  | Description                     |
|-----------|----------------------------------|
| `>`       | Redirect stdout (overwrite)      |
| `>>`      | Redirect stdout (append)         |
| `<`       | Redirect input from file         |
| `<<`      | Here document input              |
| `|`       | Pipe output to another command   |
| `||`      | OR operator (runs if previous fails) |
| `&&`      | AND operator (runs if previous succeeds) |
| `&`       | Run command in background        |
| `2>`      | Redirect stderr                  |
| `1>`      | Redirect stdout                  |
##### Here Document Example:
```bash
cat <<EOF
Hello, $USER
Welcome to automated scripting!
EOF
```
#### 🚪 Exit Codes
Exit codes are numeric signals returned by a command or script indicating its result:
| Code  | Meaning                         |
|-------|----------------------------------|
| `0`   | Success                          |
| `1-255` | Various errors or failures     |
| `$?`  | Exit code of the last command    |

Example:
```bash
some_command
echo $?   # Display the exit status of 'some_command'
```
#### 🧰 Built-In and Utility Commands
Linux scripts can leverage built-in shell commands and external utilities for automation and data processing:
| Category            | Examples                                                    |
|---------------------|-------------------------------------------------------------|
| **Shell Built-ins** | `echo`, `read`, `source`, `exit`, `test`                    |
| **Text Processing** | `awk`, `sed`, `tr`, `cut`, `wc`, `tee`, `head`, `tail`      |
| **Search & Filter** | `grep`, `egrep`, `find`, `xargs`                            |

Common usage:
```bash
# Read user input
read name
echo "Hello, $name"

# Filter lines containing "error"
grep "error" logfile.txt | tee errors.log

# Extract first column
cut -d',' -f1 data.csv | sort | uniq
```
#### 🌍 Environment Variables
Environment variables provide dynamic values used by the shell and scripts. They influence behavior and access to system-specific data.
| Variable   | Description                                      |
|------------|--------------------------------------------------|
| `$PATH`    | List of directories the shell searches for executables |
| `$SHELL`   | The user's default shell interpreter             |
| `$?`       | Exit status of the most recently executed command |
##### Example Usage:
```bash
echo "Shell in use: $SHELL"

# Check if previous command succeeded
if [ $? -eq 0 ]; then
  echo "Command executed successfully!"
else
  echo "There was an error."
fi
```
#### 🗂️ File Path Types
Understanding file path types ensures scripts reliably locate and access resources.
| Path Type     | Description                                               | Example                                 |
|---------------|-----------------------------------------------------------|-----------------------------------------|
| **Relative**  | Based on the current working directory                    | `../scripts/cleanup.sh`                 |
| **Absolute**  | Full path from the root of the filesystem                 | `/home/arthur/scripts/cleanup.sh`       |

Relative paths are flexible within a directory structure, while absolute paths guarantee location consistency across environments.
## 3.2 Given a scenario, perform basic container operations
Containers allow lightweight and portable application environments. Here’s how to perform essential container and image tasks using Docker.
### 🛠️ Container Management
| Operation         | Command Example                                       |
|-------------------|--------------------------------------------------------|
| **Start a container**     | `docker start mycontainer`                             |
| **Stop a container**      | `docker stop mycontainer`                              |
| **List running containers** | `docker ps`                                           |
| **List all containers**     | `docker ps -a`                                        |
| **Inspect container details** | `docker inspect mycontainer`                       |
| **Deploy existing image**     | `docker run -d --name webapp nginx`                |
| **Connect to container shell** | `docker exec -it mycontainer bash`               |
| **View container logs**       | `docker logs mycontainer`                         |
| **Expose ports**             | `docker run -p 8080:80 nginx`                      |
### 🖼️ Container Image Operations
| Operation        | Command Example                                      |
|------------------|------------------------------------------------------|
| **Build image from Dockerfile** | `docker build -t myimage .`                    |
| **Push image to registry**      | `docker push username/myimage`                 |
| **Pull image from registry**    | `docker pull alpine`                           |
| **List local images**           | `docker images`                                |
| **Remove image**                | `docker rmi myimage`                           |
### 🧪 Example Workflow: Simple Web Container
```bash
# Pull nginx image
docker pull nginx

# Run container and expose port 8080
docker run -d --name webserver -p 8080:80 nginx

# View logs
docker logs webserver

# Connect to container
docker exec -it webserver bash

# Stop and remove container
docker stop webserver
docker rm webserver
```
## 3.3 Given a scenario, perform basic version control using Git
Git helps track changes, collaborate efficiently, and manage project versions. Here's a concise guide to key Git operations using Markdown format.
### 🔃 Cloning Repositories
Download a remote Git repository to your local machine:
```bash
git clone https://github.com/user/project.git
```
### 📤 Pushing and 📥 Pulling Changes
Manage syncing between local and remote repositories:
- **Push** – Upload your local commits to a remote branch:
```bash
git push origin main
```
- **Pull** – Fetch and merge remote changes into your local branch:
```shell
git pull origin main
```
### ✍️ Staging and Committing Changes
Prepare and record updates in your Git repository:
- **Add files to staging:**
```bash
git add file.txt         # Stage a specific file
git add .                # Stage all changes
```
- **Commit staged changes with a message:**
```shell
git commit -m "Add feature to login page"
```
You can also amend the last commit:
```shell
git commit --amend -m "Updated login feature with validation"
```
### 🚀 Branching and Switching
Branches allow you to work on isolated features, fixes, or experiments without affecting the main codebase.
- **Create a new branch:**
```bash
git branch feature-auth
```
- **Switch to an existing branch:**
```shell
git checkout feature-auth
git checkout main
```
- **Create and switch in one step:**
```shell
git checkout -b feature-auth
```
### 🏷️ Tagging Releases
Tags identify specific points in a repository’s history—ideal for marking stable versions, releases, or milestones.
- **Create a lightweight tag:**
```bash
git tag v1.0.0
```
- **Create an annotated tag (recommended for releases):**
```shell
git tag -a v1.1.0 -m "First stable release"
```
- **List all tags in the repository:**
```shell
git tag
```
### 🚫 Ignoring Files
Using a `.gitignore` file helps keep your Git repository clean by excluding files and directories that shouldn't be tracked—such as temporary files, build artifacts, and dependencies.
#### Sample `.gitignore`
```shell
# Logs and temporary files
*.log
*.tmp

# Build artifacts
dist/
*.out

# IDE and OS files
.DS_Store
*.swp

# Dependency folders
node_modules/

# Python cache
pycache/ *.pyc

# Docker files
*.env docker-compose.override.yml
```
## 3.4 Summarize common infrastructure as code technologies
Infrastructure as Code allows system configurations, environments, and deployments to be automated, versioned, and treated like code. Here's a concise breakdown of common components.
### 📄 File Formats
IaC tools use structured, human-readable files to define infrastructure:
| Format | Description                                                         |
|--------|---------------------------------------------------------------------|
| **YAML** | "YAML Ain’t Markup Language" – popular for Ansible, CI/CD pipelines |
| **JSON** | Lightweight data format used by Terraform and other APIs           |

Example YAML:
```yaml
name: Deploy Webserver
hosts: web
tasks:
  - name: Install nginx
    apt:
      name: nginx
      state: present
```
### 🔧 IaC Utilities
Infrastructure as Code tools help automate configuration, provisioning, and deployment tasks across environments.
| Tool          | Description                                                                |
|---------------|----------------------------------------------------------------------------|
| **Ansible**   | Agentless; uses SSH and YAML playbooks to define roles and tasks           |
| **Puppet**    | Declarative; uses its own DSL and a master-agent architecture              |
| **Chef**      | Ruby-based DSL; suitable for complex workflows and infrastructure changes  |
| **SaltStack** | Event-driven; supports remote execution and state enforcement              |
| **Terraform** | Declarative; cloud-agnostic provisioning using `.tf` configuration files   |
### 🚀 CI/CD Integration
Continuous Integration and Continuous Deployment (CI/CD) streamline delivery by automating build, test, and release workflows.
#### 🔄 Common Use Cases
- Automatically apply Terraform plans after code changes
- Run Ansible playbooks upon successful merge
- Enforce config drift detection via scheduled pipelines
- Integrate with GitHub Actions, GitLab CI/CD, Jenkins, etc.

Example (GitHub Actions + Terraform):
```yaml
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Deploy with Terraform
        run: terraform apply -auto-approve
```
### 🧠 Advanced Git Topics
Mastering advanced Git workflows helps improve collaboration, maintain cleaner commit histories, and streamline reviews—especially in infrastructure projects and CI/CD pipelines.
| Concept        | Description                                                  | Example Command                    |
|----------------|--------------------------------------------------------------|------------------------------------|
| **merge**      | Integrate changes from one branch into another, preserving history | `git merge feature-branch`     |
| **rebase**     | Move or replay commits from one branch onto another for a cleaner history | `git rebase main`          |
| **pull request** | Request to merge changes via code review, typically in platforms like GitHub, GitLab, Bitbucket | Managed via web UI or CLI tools like `gh pr create` |
#### Merge vs. Rebase:
- **Merge** keeps full commit history and shows branches were combined.
- **Rebase** flattens commit history, making it linear and tidy—but can overwrite history if misused.
## 3.5 Summarize container, cloud, and orchestration concepts
This overview highlights essential technologies that support scalable infrastructure, efficient deployments, and cloud-native applications.
### ⚙️ Kubernetes Overview
Kubernetes (K8s) automates deployment, scaling, and management of containerized applications.
#### ✅ Benefits
- Self-healing: Automatically restarts failed containers
- Scaling: Dynamically adjusts replicas based on demand
- Rolling updates: Zero downtime deployments
- Declarative configuration: YAML manifests define desired state
#### 🧩 Key Components
| Component             | Description                                                |
|----------------------|------------------------------------------------------------|
| **Pod**              | Smallest deployable unit; can contain one or more containers |
| **Sidecar**          | Helper container that shares context (e.g., logging proxy, data sync) |
| **Ambassador container** | Acts as an API gateway or proxy to external systems         |
### 🖥️ Single-Node & Multicontainer Use Cases
**Docker Compose** is ideal for local development and simple deployments:

```yaml
version: "3"
services:
  web:
    image: nginx
    ports:
      - "8080:80"
  db:
    image: postgres
    environment:
      POSTGRES_PASSWORD: example
```
- Compose defines multiple services in one YAML file
- Supports linking, shared volumes, and environment variables
### 💾 Container Persistent Storage
Containerized applications often need persistent storage to retain data beyond container lifecycle events (e.g., restarts, deletions).
| Method               | Description                                                      |
|----------------------|------------------------------------------------------------------|
| **Volumes**          | Managed by the container runtime; decoupled from containers      |
| **Bind Mounts**      | Direct mapping to a host directory for more control              |
| **Persistent Volumes (PV)** | Kubernetes abstraction for durable, shared storage resources |
#### Docker Example:
```bash
# Create a named volume
docker volume create mydata

# Use the volume in a container
docker run -v mydata:/app/data myimage
```
### 🌐 Container Networking
Containers require virtualized networking to communicate internally and externally. Different models offer varying levels of isolation and flexibility.
| Network Type           | Description                                                       |
|------------------------|--------------------------------------------------------------------|
| **Overlay Network**    | Creates a virtual network that spans multiple hosts (used in orchestration tools like Docker Swarm and Kubernetes) |
| **Bridge Network**     | Default Docker network that connects containers on the same host via an internal subnet |
| **NAT (Port Mapping)** | Maps a host port to a container port, enabling external access      |
| **Host Network**       | Shares the host’s network stack; can improve performance but reduces isolation |
#### Example: Exposing a Web App
```bash
# Run a container with NAT port mapping
docker run -d -p 8080:80 nginx

# Create a custom bridge network and attach a container
docker network create mybridge
docker run -d --name webapp --network mybridge nginx
```
### 🔄 Service Mesh
A service mesh is a dedicated infrastructure layer that manages service-to-service communication in microservice architectures.
#### ✨ Key Features
| Feature            | Function                                                       |
|--------------------|----------------------------------------------------------------|
| **Traffic Routing**| Advanced control with load balancing, retries, timeouts        |
| **Security**       | Mutual TLS for encrypted connections between services          |
| **Observability**  | Metrics, distributed tracing, and logging                      |
| **Resilience**     | Circuit breaking, failovers, and retry policies                |

Popular service mesh technologies include:
- **Istio** – Full-featured mesh with advanced traffic policies and integrations
- **Linkerd** – Lightweight and performance-focused
- **Consul Connect** – Integrates with HashiCorp stack; service discovery + mesh
### 🚀 Bootstrapping with Cloud-Init
**Cloud-init** automates configuration tasks when a cloud instance first boots. Supported by major cloud platforms (e.g., AWS, Azure, OpenStack).
#### 🧰 Common Tasks
- Set hostname and timezone
- Add users and SSH keys
- Install packages and enable services
- Configure disks and networking
#### Example:
```yaml
#cloud-config
users:
  - name: deployer
    sudo: ALL=(ALL) NOPASSWD:ALL
    ssh-authorized-keys:
      - ssh-rsa AAAAB3Nza...
packages:
  - docker
runcmd:
  - systemctl enable docker
  - systemctl start docker
```
### 📥 Container Registries
Container registries act as centralized hubs for storing, sharing, and distributing container images. These registries enable teams to version, test, and deploy containerized applications seamlessly across environments.
#### 🗃️ Types of Registries
| Registry                     | Description                                        |
|------------------------------|----------------------------------------------------|
| **Docker Hub**               | Default public registry for Docker, widely supported |
| **GitHub Container Registry**| Integrates with GitHub repositories and workflows  |
| **Private Registries**       | Self-hosted or cloud-managed; used for internal images and access control |
#### 🔁 Image Lifecycle Workflow
Common tasks to manage images with registries:
```bash
# Build an image from a Dockerfile
docker build -t myapp:v1 .

# Tag image for a specific registry
docker tag myapp:v1 ghcr.io/username/myapp:v1

# Push image to the registry
docker push ghcr.io/username/myapp:v1

# Pull an image from the registry
docker pull nginx
```
#### 🔐 Securing Registries
Container registries must be secured to protect image integrity, control access, and prevent unauthorized usage or tampering.
##### 🔒 Security Practices
| Practice                     | Description                                               |
|------------------------------|-----------------------------------------------------------|
| **Authentication**          | Require login credentials or access tokens                |
| **TLS Encryption**          | Use HTTPS to encrypt image transfers                      |
| **Access Control Lists (ACLs)** | Restrict who can push/pull/tag images                |
| **Image Scanning**          | Detect vulnerabilities using tools like Trivy or Clair    |
| **Signing and Verification**| Ensure image integrity using tools like Cosign or Notary  |
##### 🔐 Example: Authenticating and Pushing Securely
```bash
# Log in to container registry
docker login ghcr.io

# Push signed and scanned image
docker push ghcr.io/username/myapp:v1
```
# 4.0 Troubleshooting
## 4.1 Given a scenario, analyze and troubleshoot storage issues
Analyzing storage performance and reliability requires understanding latency, capacity, hardware behaviors, and filesystem integrity.
### 🐢 High Latency
| Symptom      | Diagnostic Tool       | Potential Cause                         |
|--------------|------------------------|------------------------------------------|
| High I/O wait| `iostat`, `vmstat`, `top` | Disk under load, slow media response    |
#### Suggested Actions
- Check disk speed with `hdparm`
- Investigate running processes causing bottlenecks
- Ensure proper disk scheduling (`noop` for SSDs)
### 📉 Low Throughput
| Symptom         | Tools                  | Common Causes                    |
|------------------|------------------------|----------------------------------|
| Slow read/write speeds | `dd`, `fio`, `iostat`  | Bandwidth saturation, RAID misconfig, filesystem overhead |
#### Suggested Actions
- Run benchmark: `dd if=/dev/zero of=testfile bs=1M count=1024 oflag=direct`
- Check RAID health and caching
- Use appropriate filesystem for workload (e.g., XFS for large files)
### 🧮 IOPS Issues
| Symptom   | Diagnostic Tools     | Likely Causes                         |
|-----------|----------------------|----------------------------------------|
| Low IOPS  | `iostat -x`, `fio`   | SSD aging, controller limits, scheduler choice |
#### Suggested Actions
- Switch to `noop` or `deadline` scheduler for SSD
- Monitor trim usage with `fstrim` and check support
- Use RAID 10 for better IOPS if applicable
### 💾 Capacity Issues
| Issue           | Diagnosis                      | Fix                                      |
|------------------|-------------------------------|------------------------------------------|
| Low disk space   | `df -h`, `du -sh /*`           | Delete unused files, increase disk size  |
| Inode exhaustion | `df -i`, `find / -xdev`        | Remove excessive tiny files, change inode density |
### 📁 Filesystem Issues
| Type         | Symptom                              | Diagnostic Tool        | Resolution                          |
|--------------|----------------------------------------|------------------------|--------------------------------------|
| Corruption   | Read errors, failed mounts            | `fsck`, `dmesg`        | Repair with `fsck`, restore from backup |
| Mismatch     | Mount errors, missing files           | `/etc/fstab`, `blkid` | Correct labels/UUIDs and `fstab` entries |
### ⏱️ I/O Scheduler
Schedulers affect disk access efficiency. View and change using:
```bash
cat /sys/block/sdX/queue/scheduler
echo deadline > /sys/block/sdX/queue/scheduler
```
- `noop`: Best for SSDs (no reordering)
- `deadline`: Reduces latency
- `cfq`: Fair scheduler for mixed workloads
### 🔧 Device-Level Issues
Storage hardware can exhibit performance degradation, data integrity issues, or complete failure. Regular diagnostics and maintenance are key to avoiding surprises.
#### 📘 Common Devices and Diagnostics
| Device Type         | Tools/Commands                            | Issue Examples                        |
|---------------------|-------------------------------------------|----------------------------------------|
| **NVMe / SSD**      | `smartctl -a`, `nvme list`                | High wear level, overheating, bad blocks |
| **SSD Trim**        | `fstrim -v /`                              | Inefficient space reuse, slow writes    |
| **RAID Arrays**     | `cat /proc/mdstat`, `mdadm --detail`      | Rebuild errors, degraded state          |
| **LVM (Logical Volumes)** | `lvdisplay`, `vgdisplay`, `pvscan`       | Volume full, metadata errors           |
| **I/O Errors**      | `dmesg`, `smartctl`, `journalctl`         | Read/write failures, device disconnects |
#### 🔍 Sample Troubleshooting
```bash
# Check NVMe health
nvme smart-log /dev/nvme0

# Display RAID array status
cat /proc/mdstat

# Run a quick SMART check on disk
smartctl -H /dev/sda

# View recent I/O errors from kernel messages
dmesg | grep -i error
```
### 🧱 Mount Option Problems
Mount options determine how filesystems behave during read/write operations, directly influencing performance, reliability, and system behavior.
#### 🚩 Common Mount Options and Their Impacts
| Option     | Effect                                              | Recommendation                                  |
|------------|-----------------------------------------------------|-------------------------------------------------|
| `noatime`  | Disables access time updates for read operations    | Improves performance for frequent reads         |
| `sync`     | Forces synchronous writes to disk                   | Can slow performance; use `async` if safe       |
| `ro`       | Mounts filesystem as read-only                      | Intended for recovery or strict protection      |
| `rw`       | Enables read and write                              | Needed for most interactive data applications   |
| `relatime` | Updates access time less frequently                 | Balance between `noatime` and `atime` overhead  |
#### 🔍 Diagnosing Mount Problems
You can investigate current mount options and correct misconfigurations:
```bash
# View current mount points and options
mount | grep /dev/sd

# Check filesystem entries
cat /etc/fstab

# Remount with updated options
sudo mount -o remount,rw /mnt/data
```
Watch for mismatched or overly restrictive options that might cause apps to fail writing, trigger permission errors, or reduce performance.
## 4.2 Given a scenario, analyze and troubleshoot network resource issues
When analyzing network issues, it’s essential to break down problems by category—covering configuration, hardware, software, and communication paths.
### ⚙️ Network Configuration Issues
Misconfigurations can block traffic, confuse routing, or isolate devices.
#### Subnet Problems
- Incorrect subnet masks may prevent proper device communication
- Use `ip addr`, `ipcalc`, or `ifconfig` to verify subnet configuration
- Verify subnet masks across devices to ensure consistency.
- Check if devices are on the correct subnet range to avoid routing mishaps.
- Use tools like `ipconfig / ifconfig` or `ip addr` to inspect subnet settings.
#### Routing Issues
- Missing or incorrect routes lead to unreachable networks
- Check routing table: `ip route` or `netstat -rn`
- Run `traceroute` or `tracert` to spot unreachable hops.
- Use `netstat -r` or `ip route` to inspect route tables.
- Ensure default gateways are properly configured.
#### 🔍 Example:
```bash
# Display IP and route info
ip addr
ip route
```
### 🔥 Firewall Issues
Firewalls are vital for securing systems, but misconfigurations can block legitimate network traffic or hinder troubleshooting.
- Check firewall rules to confirm required ports and IPs aren’t being blocked.
- Inspect connection logs for denied traffic.
- Temporarily disable firewalls to confirm if they are the root cause (with caution and authorization).
#### 🔍 Diagnosis and Tools
| Tool/Command          | Purpose                                          |
|------------------------|--------------------------------------------------|
| `iptables -L`          | List active rules in iptables                   |
| `ufw status`           | Show status and rules in Uncomplicated Firewall (Ubuntu) |
| `firewall-cmd --list-all` | List settings for `firewalld` zones (Red Hat-based systems) |
#### 🧪 Troubleshooting Steps
```bash
# Temporarily disable firewall (use with caution)
sudo ufw disable        # Ubuntu
sudo iptables -F        # Flush iptables rules

# Check if port is being blocked
sudo iptables -L -n | grep DROP
```
- Verify that required ports (e.g. 22 for SSH, 80/443 for web) are allowed
- Use `nmap` or `telnet` to test remote connectivity
- Check logs: `journalctl`, `/var/log/syslog`, or firewall-specific logs
### 🖧 Interface Errors
Network interfaces can exhibit errors due to physical faults, driver issues, or traffic congestion. Monitoring their health is vital for diagnosing degraded connectivity.
#### ➤ Dropped Packets
- Use `netstat -s` or interface monitoring tools to check packet loss stats.
- Monitor traffic flow using Wireshark or tcpdump.
#### ➤ Collisions
- Collisions are common in half-duplex setups—ensure full-duplex configuration.
- Analyze switch port statistics via SNMP or dashboard tools.
#### ➤ Link Status
- Check physical cabling and link lights on NICs and switches.
- Run `ethtool ethX` or check interface status (`ip link show`).
#### 📋 Common Interface Issues
| Issue            | Description                                       | Diagnostic Tool        |
|------------------|---------------------------------------------------|------------------------|
| **Dropped Packets** | Packets discarded due to buffer overflows or congestion | `ip -s link`, `netstat -i` |
| **Collisions**   | Frame collisions (rare in full-duplex networks)   | `ifconfig`, `ethtool` |
| **Link Status**  | Physical interface up/down, speed mismatches      | `ethtool`, `dmesg`     |
#### 🔍 Diagnostic Examples
```bash
# Check interface statistics
ip -s link

# Get detailed link info including speed and duplex
ethtool eth0

# View recent hardware-related messages
dmesg | grep eth
```
### 📉 Bandwidth Limitations & High Latency
Network slowness and lag often stem from bandwidth congestion, inefficient routing, or hardware constraints.
#### ➤ High Latency
- Ping targets multiple times and compare response times.
- Run continuous `ping` or `mtr` to analyze jitter and delay.
- Check for congestion using bandwidth monitoring tools like `iftop`, `nload`, or NetFlow.
#### ⚠️ Common Causes
| Issue             | Description                                             | Detection Tools          |
|-------------------|---------------------------------------------------------|--------------------------|
| High latency      | Delayed packet delivery across network paths            | `ping`, `mtr`            |
| Bandwidth caps    | Provider or hardware-enforced speed limits              | `iperf3`, `bmon`         |
| Congestion        | Excessive simultaneous traffic on interfaces            | `iftop`, `nload`         |
#### 🧪 Diagnostic Tools and Usage
```bash
# Measure latency and packet loss
ping -c 10 example.com

# Run real-time traceroute with latency metrics
mtr -rw example.com

# Benchmark actual bandwidth between hosts
iperf3 -s          # Run as server on remote host
iperf3 -c remote-IP  # Run client test

# Monitor live bandwidth usage
sudo apt install bmon
bmon
```
Latency can also fluctuate based on routing paths or physical distance between nodes. Use traceroute-style tools like mtr to inspect hops and delays.
### 🌐 Name Resolution Issues
#### ➤ DNS
- Use `nslookup` or `dig` to test resolution of internal and external domains.
- Confirm DNS server configuration and availability.
- Try alternate DNS servers (Google: 8.8.8.8, Cloudflare: 1.1.1.1) to isolate problems.
### 🧪 Testing Remote Systems
#### ➤ Nmap
- Scan ports/services using `nmap -Pn <host>` for reachability.
- Use `nmap -sV` to identify running services and versions.
#### ➤ openssl s_client
- Test SSL connectivity with:
```shell
openssl s_client -connect <host>:443
```
- Review certificate validity, supported cipher suites, and TLS handshake.
## 4.3 Given a scenario, analyze and troubleshoot central processing unit (CPU) and memory issues
### 🧵 Process-Related Issues
#### ➤ Runaway Processes
- Identify with `top`, `htop`, or `ps aux --sort=-%cpu`.
- Look for abnormally high CPU/memory usage and investigate the command/process logic.
- Kill or restart the offending process using `kill -9 <pid>` or `systemctl`.
#### ➤ Zombie Processes
- Use `ps aux | grep Z` or check `STAT` column in `top`.
- Usually harmless unless excessive—reboot or fix parent process to collect zombie status.
### 📈 CPU Load & Utilization
#### ➤ High CPU Utilization
- Analyze using `top` or `mpstat`.
- Identify real-time CPU hogs and validate whether it’s expected workload.
#### ➤ High Load Average
- Check using `uptime` or `top`.
- Compare load against available cores (e.g., 4-core system should keep under ~4.0).
- Assess whether it's CPU-bound or IO-bound using `iostat`, `vmstat`.
#### ➤ High Run Queues
- Use `vmstat 1` and examine the `r` column.
- Indicates how many processes are waiting for CPU time—may signal contention.
### ⏱ CPU Time Metrics
| Time    | Meaning                                 |
|---------|-----------------------------------------|
| user    | Time spent on user-level processes      |
| system  | Time in kernel space                    |
| idle    | CPU not being used                      |
| iowait  | CPU waiting on I/O                      |
| steal   | Time stolen by hypervisor (VMs)         |

- Use `mpstat -P ALL` or `sar` to visualize these stats per core.
### 🎚 CPU Priorities
#### ➤ nice / renice
- Control scheduling priority with `nice -n <level> <command>` (lower = higher priority).
- Adjust running processes with `renice -n <level> -p <pid>`.
### 🧠 Memory Management
#### ➤ Memory Exhaustion
- Use `free -m`, `vmstat`, or `top` to compare free memory vs. file cache.
- Linux may show low "free" memory but high cache—this is normal unless swap kicks in.
#### ➤ Out Of Memory (OOM)
- Look in `/var/log/syslog` or `dmesg | grep -i 'killed process'`.
- Linux OOM killer terminates low-priority/high-consuming processes.
- Investigate with tools like `smem` or `ps_mem`.
#### ➤ Memory Leaks
- Spot long-lived processes gradually consuming more memory (e.g., via `top`, `ps`).
- Use tools like `valgrind` or language-specific profilers (Python: `objgraph`, Java: `VisualVM`).
### 🔄 Swapping
- Excessive swap usage = performance hit.
- Check with `swapon -s`, `vmstat`, `free -m`.
- Consider tuning vm.swappiness in `/etc/sysctl.conf`.
### 🔧 Hardware Inspection
| Command          | Function                        |
|------------------|---------------------------------|
| `lscpu`          | CPU architecture & specs        |
| `lsmem`          | Detailed memory info            |
| `/proc/cpuinfo`  | Raw CPU details per core        |
| `/proc/meminfo`  | Memory usage breakdown          |

These give a full view of hardware topology, helpful for identifying limits and misconfiguration.
## 4.4 Given a scenario, analyze and troubleshoot user access and file permissions
### 🔑 User Login Issues
- Check authentication method: Local, LDAP, Kerberos, etc.
- Inspect logs: `/var/log/auth.log` or `/var/log/secure` for failed logins.
- Use `last` and `who` to verify login activity.
- Validate home directory, shell access, and account status (`passwd -S <user>`).
### 🗂️ User File Access Issues
#### ➤ Group
- Confirm user group membership via `groups <username>` or `id`
- Check file group ownership with `ls -l`.
- Add users to groups using `usermod -aG <group> <user>`.
#### ➤ Context (SELinux/AppArmor)
- In SELinux environments, inspect with `ls -Z`, and manage with `chcon`.
- For AppArmor, check profile enforcement and logs in `/var/log/syslog`.
#### ➤ Permission
- Use `ls -l` for standard permissions (rwx).
- Correct with `chmod` (e.g., `chmod 644 file.txt`).
- Ensure the effective UID/GID can access the file.
#### ➤ ACL (Access Control Lists)
- View ACLs with `getfacl file.txt`.
- Set granular permissions with `setfacl -m u:username:rwx file.txt`.
- Remove with `setfacl -x u:username file.txt`.
#### ➤ Attribute
- Immutable or append-only files can be checked via `lsattr`.
- Use `chattr -i` or `chattr -a` to modify if access denied.
#### ➤ Policy vs. Non-Policy
- Review system-wide policies via PAM, audit rules, or security frameworks.
- Confirm no conflicting policies that override expected behavior.
### 🔐 Password Issues
- Force reset with `passwd <user>`.
- Check password aging and expiration via `chage -l <user>`.
- Inspect PAM configuration (`/etc/pam.d/`) for policy enforcement.
### 🧰 Privilege Elevation
- Confirm sudo privileges: `sudo -l` or examine `/etc/sudoers`.
- Use `visudo` for safe edits.
- For temporary elevation: `su - <user>` or sudoers configuration.
### 📊 Quota Issues
- Check quotas with `quota -u <user>` and `repquota -a`.
- Inspect disk usage: `du -sh ~` or `df -h`.
- Configure quotas via `edquota` and verify with mount options (`usrquota`, `grpquota`).
