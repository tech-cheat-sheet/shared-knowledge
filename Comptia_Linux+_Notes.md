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
