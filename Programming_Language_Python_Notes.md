- [Python - How to install](#python---how-to-install)
- [Python - Useful Commands](#python---useful-commands)
  - [Problem - externally-managed-environment](#problem---externally-managed-environment)
  - [Solution - externally-managed-environment](#solution---externally-managed-environment)
# Python - How to install
```shell
# Python3
sudo apt-get update --yes
sudo apt-get install python3 --yes
# PIP - Python Package Manager
sudo apt-get install python3-pip --yes
# Virtual Environment
sudo apt install python3-venv --yes

# Test
python3 --version
pip3 --version
```
# Python - Useful Commands
```shell
python3 --version
pip3 --version
python3 -m pip --version

# Upgrade
python3 -m pip install --upgrade pip
```
## Problem - externally-managed-environment
Modern Linux distros like Ubuntu 23.04+ and Debian 12 adopted PEP 668, which protects system-managed Python environments. When you try to install a package with pip outside a virtual environment, you’ll hit:
```shell
error: externally-managed-environment
× This environment is externally managed
╰─> To install Python packages system-wide, try apt install python3-xyz
```
This prevents conflicts between pip-installed packages and those managed by your OS’s package manager (like apt).
## Solution - externally-managed-environment
On Linux distribution like Ubuntu or CentOS/RHEL, their respective package manager:

- Ubuntu=APT
- CentOS/RHEL=YUM

are dependent on Python, so we must use virtual environment:
```shell
# Create a new virtual environment and activate it
python3 -m venv myenv
source myenv/bin/activate
# To deactivate
deactivate
# Check activated venv
echo $VIRTUAL_ENV
which python3
# Above, if there is one venv activated, you should see something like: 
/home/arthur/myenv/bin/python
# If not: 
/usr/bin/python3
```