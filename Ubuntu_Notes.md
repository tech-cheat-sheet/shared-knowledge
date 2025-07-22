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
- [Ubuntu Support](#ubuntu-support)
  - [Types](#types)
  - [Extended Security Maintenance (ESM)](#extended-security-maintenance-esm)
    - [🧠 Why Use ESM?](#-why-use-esm)
  - [🆚 Ubuntu Support Comparison](#-ubuntu-support-comparison)
  - [🗂️ Ubuntu Repository Comparison](#️-ubuntu-repository-comparison)
    - [🧠 Quick Summary](#-quick-summary)
    - [List all installed packages from Universe/Multiverse repo - CLI](#list-all-installed-packages-from-universemultiverse-repo---cli)
    - [How to Exclude *lib* packages from results](#how-to-exclude-lib-packages-from-results)
    - [List all installed packages from Universe/Multiverse repo - SCRIPT](#list-all-installed-packages-from-universemultiverse-repo---script)
    - [Delete/Remove/Uninstall Universe/Multiverse Packages](#deleteremoveuninstall-universemultiverse-packages)
    - [1. View All Active Repositories](#1-view-all-active-repositories)
    - [2. Use apt-cache policy for a Detailed View](#2-use-apt-cache-policy-for-a-detailed-view)
      - [📁 Package Sources Summary (`apt-cache policy`)](#-package-sources-summary-apt-cache-policy)
      - [🧠 How Priority Works](#-how-priority-works)
      - [🔍 Repository Sections Explained](#-repository-sections-explained)
      - [🛡️ Security Updates](#️-security-updates)
    - [📁 3. List Only External PPAs](#-3-list-only-external-ppas)
    - [🧪 4. Filter for Specific Repos (e.g., Universe or Multiverse)](#-4-filter-for-specific-repos-eg-universe-or-multiverse)
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
# Ubuntu Support
## Types
There are 2 types of Ubuntu releases: Interim and LTS. Each Ubuntu LTS is maintained for 10 years total: 5 years of standard support + 5 years of ESM. Interim releases are maintained for 9 months.
## Extended Security Maintenance (ESM)
Extended Security Maintenance (ESM) is a service provided by Canonical that extends the life of Ubuntu Long-Term Support (LTS) releases beyond their standard 5-year support window.
| Feature             | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| **Extended Support**| Adds up to 5 extra years of security updates after standard LTS ends         |
| **Package Coverage**| Includes updates for both **Main** and **Universe** repositories             |
| **Livepatching**    | Enables kernel updates **without rebooting**, reducing downtime              |
| **Compliance Ready**| Helps meet standards like **HIPAA, GDPR, FIPS 140-2**                        |
| **Access Methods**  | Available via **Ubuntu Pro**, **Ubuntu Advantage**, or **cloud platforms**  |
| **Free Tier**       | Free for up to **5 personal machines** and **50 for Ubuntu community members** |

### 🧠 Why Use ESM?
- Keeps older Ubuntu systems secure and compliant without immediate upgrades
- Ideal for legacy applications, regulated industries, or long-term deployments
- Lets you plan upgrades at your own pace while maintaining protection

Sources:
- https://releases.ubuntu.com/

## 🆚 Ubuntu Support Comparison
| Feature             | 🛠️ Ubuntu Standard Support                              | 🚀 Ubuntu Pro Support                                         |
|---------------------|----------------------------------------------------------|---------------------------------------------------------------|
| **Support Duration**| 5 years (LTS releases only)                               | Up to 10 years (LTS releases)                                 |
| **Package Coverage**| Security updates for **main** repository only            | Security updates for **main + universe** (25,000+ packages)   |
| **Compliance Tools**| No built-in compliance support                           | Supports **HIPAA, GDPR, FIPS 140-2**, and more                |
| **Livepatch Support**| ❌ Not included — kernel updates require reboot         | ✅ Included — patch kernel without reboot                      |
| **Support Channels**| Community forums, optional paid support                  | Canonical enterprise-grade support (self-service or 24/7)     |
| **Best Use Case**   | Personal machines, developers, non-critical projects     | Business-critical systems, enterprise, regulated industries   |
| **Free Tier**       | Always free                                               | Free for **up to 5 personal machines**                        |

## 🗂️ Ubuntu Repository Comparison
| Repository     | License Type         | Maintained By       | Support Level           | Contains                                  |
|----------------|----------------------|----------------------|--------------------------|-------------------------------------------|
| **Main**        | Free & Open Source   | Canonical            | ✅ Fully supported        | Core OS packages, officially vetted apps  |
| **Restricted**  | Proprietary          | Canonical            | ✅ Supported (limited)    | Essential proprietary drivers (e.g. GPU)  |
| **Universe**    | Free & Open Source   | Community            | ⚠️ Community-supported    | Thousands of community-maintained apps    |
| **Multiverse**  | Proprietary / Mixed  | Community            | ❌ Unsupported            | Software with legal or licensing issues   |
### 🧠 Quick Summary
- Main: Safe, stable, and officially maintained — ideal for production systems.
- Restricted: Necessary proprietary drivers with Canonical support.
- Universe: Huge library of open-source tools, but updates aren’t guaranteed.
- Multiverse: Use with caution — includes codecs, games, and other non-free software.

Sources:
- https://ubuntu.com/about/release-cycle
### List all installed packages from Universe/Multiverse repo - CLI
Prerequisite
```shell
sudo apt install --yes aptitude
```

```shell
aptitude search -F "%p" "~i ?section(universe)"
aptitude search -F "%p" "~i ?section(multiverse)"
```
- `~i` filters for installed packages
- `?section(universe)` limits results to Universe repo
- `%p` prints package names only
### How to Exclude *lib* packages from results
```shell
# list all installed packages from the Universe repository excluding those with lib in their name
aptitude search -F "%p" "~i ?section(universe)" | grep -v lib

# exclude packages that start with lib
aptitude search -F "%p" "~i ?section(universe)" | grep -v '^lib'
```
- `aptitude search -F "%p" "~i ?section(universe)` lists all installed packages from Universe
- `grep -v lib` filters out any package names that contain the string lib
- This is a simple string match, so it will exclude any package with lib anywhere in its name—whether it's a library or not.
### List all installed packages from Universe/Multiverse repo - SCRIPT
```shell
for pkg in $(dpkg-query -W -f='${Package}\n'); do
  apt-cache policy "$pkg" | grep -q 'universe' && echo "$pkg"
  apt-cache policy "$pkg" | grep -q 'multiverse' && echo "$pkg"
done
```
### Delete/Remove/Uninstall Universe/Multiverse Packages
```shell
sudo apt purge $(aptitude search -F "%p" "~i ?section(universe)")
sudo apt purge $(aptitude search -F "%p" "~i ?section(multiverse)")
```
### 1. View All Active Repositories
```shell
grep -rhE ^deb /etc/apt/sources.list /etc/apt/sources.list.d/
```
- This shows all active deb entries (binary package sources).
- It includes both official Ubuntu repos and any third-party PPAs.
### 2. Use apt-cache policy for a Detailed View
```shell
apt-cache policy
```
- Lists all repositories and their priorities.
- Useful for checking which repo a package will be pulled from.
#### 📁 Package Sources Summary (`apt-cache policy`)
This tells you where packages and updates come from, and what priority each source has when installing or updating software.
| Priority | Source URL                                             | Repository Info                                                                 |
|----------|--------------------------------------------------------|----------------------------------------------------------------------------------|
| 500      | http://security.ubuntu.com/...                         | Official Ubuntu security updates: main, universe, restricted, multiverse        |
| 500      | http://ca.archive.ubuntu.com/...                       | Base Ubuntu repositories: noble main, universe, restricted, multiverse          |
| 100      | http://ca.archive.ubuntu.com/ubuntu noble-backports/...| Lower-priority backport packages (main and universe)                            |
| 500      | https://pkgs.k8s.io/...                                | Kubernetes packages from openSUSE Build Service                                 |
| 500      | https://download.docker.com/...                        | Docker CE stable repository                                                      |
| 100      | /var/lib/dpkg/status                                   | Locally installed packages not tied to a repository                              |

#### 🧠 How Priority Works
APT assigns numeric priorities to determine which source wins during installation:
- `500` is standard for online repositories
- `100` is typical for backports or manually installed packages
- Higher numbers override lower ones
- You could "pin" packages to increase or decrease preference, but your system currently shows no pinned packages
#### 🔍 Repository Sections Explained
- `main` → Officially supported software by Canonical
- `universe` → Community-maintained open-source packages
- `restricted` → Supported but proprietary packages (e.g. drivers)
- `multiverse` → Software with licensing restrictions (e.g. codecs, fonts)
#### 🛡️ Security Updates
The `noble-security` entries show that your system is set to receive timely security patches from `security.ubuntu.com`, which is great practice.
### 📁 3. List Only External PPAs
```shell
ls /etc/apt/sources.list.d/
```
- This directory contains `.list` files for added PPAs and third-party sources.
To view their contents:
```shell
cat /etc/apt/sources.list.d/*.list
```
### 🧪 4. Filter for Specific Repos (e.g., Universe or Multiverse)
```shell
grep -rhE ^deb /etc/apt/sources.list* | grep universe
grep -rhE ^deb /etc/apt/sources.list* | grep multiverse
```
