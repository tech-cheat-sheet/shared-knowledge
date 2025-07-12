- [How to install Docker](#how-to-install-docker)
  - [Uninstall all conflicting packages:](#uninstall-all-conflicting-packages)
  - [Add Docker's official GPG key:](#add-dockers-official-gpg-key)
  - [Add the repository to Apt sources:](#add-the-repository-to-apt-sources)
  - [Install the Docker packages](#install-the-docker-packages)
  - [Verify](#verify)
- [A Shipping Analogy for Docker, Kubernetes, and Helm](#a-shipping-analogy-for-docker-kubernetes-and-helm)
  - [Docker: The Shipping Container](#docker-the-shipping-container)
  - [Kubernetes: The Port \& Crane System](#kubernetes-the-port--crane-system)
  - [Helm: The Shipping Manifest \& Blueprint](#helm-the-shipping-manifest--blueprint)
# How to install Docker
https://docs.docker.com/engine/install/ubuntu/
## Uninstall all conflicting packages:
for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done
## Add Docker's official GPG key:
```shell
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
```
## Add the repository to Apt sources:
```shell
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
## Install the Docker packages
```shell
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
## Verify
```shell
sudo docker run hello-world
```

<!-- '# A Shipping Analogy for Docker, Kubernetes, and Helm' BEGIN -->
# A Shipping Analogy for Docker, Kubernetes, and Helm
## Docker: The Shipping Container
- Think of Docker as a standardized shipping container.
- You pack your application and all its dependencies into one container so it can travel anywhere—on a truck, train, or ship—without missing a thing.
## Kubernetes: The Port & Crane System
- Kubernetes is like a busy seaport with cranes, docks, and logistics staff.
- It schedules containers (your “boxes”) onto ships (nodes), moves them between warehouses (pods), and keeps everything running smoothly—adding more cranes when traffic spikes and replacing broken ones automatically.
## Helm: The Shipping Manifest & Blueprint
- Helm serves as the shipping manifest and blueprint for an entire fleet.
- Instead of detailing each container by hand, you define a chart (manifest) listing which containers go where, how many copies you need, and any special handling instructions.
- When you update your manifest and re-submit it, the port applies the changes—adding new containers or removing old ones in a controlled way.

| Role                   | Real World                       | Tool       |
|------------------------|----------------------------------|------------|
| Package a single unit  | Shipping container               | Docker     |
| Orchestrate at scale   | Port operations & scheduling     | Kubernetes |
| Manage fleet manifests | Shipping manifests & blueprints | Helm       |

With this model, you can see how each layer builds on the last: Docker standardizes your workloads, Kubernetes runs them reliably at scale, and Helm lets you version and deploy entire application “fleets” with ease.
<!-- '# A Shipping Analogy for Docker, Kubernetes, and Helm' END -->
