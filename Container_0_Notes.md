- [0. Close all opened terminals and open a new/clean one](#0-close-all-opened-terminals-and-open-a-newclean-one)
- [1. Verify what is installed](#1-verify-what-is-installed)
- [2. 🧹 Uninstall Minikube](#2--uninstall-minikube)
- [3. 🧼 Uninstall Docker](#3--uninstall-docker)
- [4. Uninstall kubectl](#4-uninstall-kubectl)
  - [5. Final checks](#5-final-checks)
# 0. Close all opened terminals and open a new/clean one
# 1. Verify what is installed
```shell
which docker
which kubectl
which minikube
```
# 2. 🧹 Uninstall Minikube
```shell
# 1. Stop the cluster
minikube stop

# 2. Delete the cluster and all associated resources
minikube delete --all --purge

# 3. Remove the Minikube binary
sudo rm -rf /usr/local/bin/minikube

# 4. Remove Minikube configuration and cache
rm -rf ~/.minikube
rm -rf ~/.kube
sudo rm -rf /usr/local/bin/kubectl
```
# 3. 🧼 Uninstall Docker
```shell
# 1. Stop and remove all containers
docker stop $(docker ps -aq)
docker rm $(docker ps -aq)

# 2. Remove all images
docker rmi $(docker images -aq)

# 3. Remove Docker packages
sudo apt-get purge -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
sudo apt-get autoremove -y
sudo apt-get autoclean

# 4. Delete Docker directories and config
sudo rm -rf /var/lib/docker /etc/docker
sudo rm -rf /var/run/docker.sock
sudo rm -rf ~/.docker
sudo groupdel docker
```
# 4. Uninstall kubectl
```shell
sudo snap remove kubectl
rm -rf ~/.kube
```
## 5. Final checks
```shell
which docker && which kubectl && which minikube
```
