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
