- [Ubuntu - Useful Commands](#ubuntu---useful-commands)
  - [Check Ubuntu Distribution](#check-ubuntu-distribution)
  - [List installed packages](#list-installed-packages)
  - [Create a new file](#create-a-new-file)
  - [Running Processes - CLI](#running-processes---cli)
  - [Running Processes - GUI](#running-processes---gui)
  - [📁 File \& Directory Management](#-file--directory-management)
  - [📄 File Viewing \& Text Processing](#-file-viewing--text-processing)
  - [🧠 System Monitoring \& Process Management](#-system-monitoring--process-management)
  - [🌐 Networking \& Remote Access](#-networking--remote-access)
  - [🔐 Permissions \& Security](#-permissions--security)
  - [📦 Package \& Dependency Management](#-package--dependency-management)
  - [👤 User \& Group Management](#-user--group-management)
  - [🧰 Shell Utilities \& Shortcuts](#-shell-utilities--shortcuts)
- [Ubuntu/Linux Graphical Package Manager:](#ubuntulinux-graphical-package-manager)
  - [🆚 App Center vs Synaptic](#-app-center-vs-synaptic)
  - [🧠 Which Should You Use?](#-which-should-you-use)
<!-- '# Ubuntu - Useful Commands' BEGIN -->
# Ubuntu - Useful Commands
## Check Ubuntu Distribution
```shell
lsb_release -a
hostnamectl
uname -r
```
## List installed packages
```shell
# APT
sudo apt list --installed
# SNAP
sudo snap list
```
## Create a new file
```shell
touch filename.txt
```
## Running Processes - CLI
```shell
# List running processes:
ps aux

# Grep process IDs by name
pgrep PROCESS_NAME

# Kill all running processes by name
pgrep PROCESS_NAME | xargs kill -9
```
## Running Processes - GUI
Linux/Ubuntu's equivalent of Windows Task Manager is called:

System Monitor

## 📁 File & Directory Management
- ls – List files and directories
- cd – Change directory
- pwd – Show current directory
- mkdir / rmdir – Create or remove directories
- cp / mv / rm – Copy, move, or delete files
- touch – Create empty files
- find / locate – Search for files
- tree – Display directory structure
## 📄 File Viewing & Text Processing
- cat / less / more – View file contents
- head / tail – Show first or last lines
- grep – Search text patterns
- awk / sed – Advanced text processing
- cut / sort / uniq / wc – Manipulate and count text
## 🧠 System Monitoring & Process Management
- top / htop – Real-time process viewer
- ps – List running processes
- kill / pkill / killall – Terminate processes
- uptime – Show system uptime
- free – Display memory usage
- df / du – Disk space usage
- lsof – List open files
- vmstat / iostat – System performance stats
## 🌐 Networking & Remote Access
- ping / traceroute – Test connectivity
- curl / wget – Fetch web content
- ssh / scp / sftp – Secure remote access and file transfer
- netstat / ss – View network connections
- ip / ifconfig – Network interface info
- nmap – Network scanner
- tcpdump – Packet capture
## 🔐 Permissions & Security
- chmod – Change file permissions
- chown / chgrp – Change ownership
- umask – Set default permissions
- sudo – Run commands as superuser
- passwd – Change user password
- gpg / openssl – Encrypt and secure files
## 📦 Package & Dependency Management
- apt / yum / dnf / pacman – Install and manage packages
- dpkg / rpm – Low-level package tools
- snap / flatpak – Universal package formats
- pip / npm / cargo – Language-specific package managers
## 👤 User & Group Management
- useradd / usermod / userdel – Manage users
- groupadd / groupdel – Manage groups
- whoami / id – Show user info
- su / sudo – Switch or elevate user
- groups – Show group memberships
## 🧰 Shell Utilities & Shortcuts
- alias / unalias – Create command shortcuts
- man / --help – Access command manuals
- history – View command history
- clear – Clean terminal screen
- echo / date / sleep – Misc utilities
- time – Measure command execution time
<!-- '# Ubuntu - Useful Commands' END -->



<!-- '# Ubuntu/Linux Graphical Package Manager:' BEGIN -->
# Ubuntu/Linux Graphical Package Manager:
Ubuntu "App Center" is mostly for Snap.
For APT, we need something like:
```shell
sudo apt install --yes gnome-software
# Note: once installed, it is called "Software"

or

sudo apt install --yes synaptic
# Note: once installed, it is called "Synaptic Package Manager"
# Sources: 
# - https://help.ubuntu.com/stable/ubuntu-help/addremove-install-synaptic.html.en
# - https://itsfoss.com/synaptic-package-manager/
```
<!-- '# Ubuntu/Linux Graphical Package Manager:' END -->
## 🆚 App Center vs Synaptic
| Feature               | Ubuntu App Center                                    | Synaptic Package Manager                            |
|------------------------|-----------------------------------------------------|-----------------------------------------------------|
| **Interface**         | Modern, clean, touch-friendly (Flutter-based)        | Classic GTK interface; utilitarian                  |
| **Ease of Use**       | Very beginner-friendly                               | Geared toward intermediate/advanced users           |
| **Package Support**   | Supports Snap & .deb (limited .deb in 22.04)         | Supports only .deb via APT                          |
| **Dependency Control**| Minimal control                                      | Full control over dependencies                      |
| **Search & Discoverability** | Ratings, screenshots, categories            | Powerful search; lacks visuals or ratings           |
| **Offline .deb Install** | ❌ Not supported (as of 22.04)                   | ✅ Fully supported                                  |
| **Advanced Features** | Basic install/update/remove                          | Includes fix broken packages, lock versions, etc.   |
| **Performance**       | Lightweight but Snap integration can lag             | Fast and responsive                                 |
## 🧠 Which Should You Use?
- Use App Center if you want a sleek, app-store-like experience and mostly install Snap packages or mainstream apps.
- Use Synaptic if you need precision, control, or want to manage system-level packages and dependencies.
