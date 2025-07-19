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
