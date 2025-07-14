- [How to install Docker on Ubuntu](#how-to-install-docker-on-ubuntu)
  - [Reference:](#reference)
  - [0. Uninstall all conflicting packages:](#0-uninstall-all-conflicting-packages)
  - [1. Add Docker's official GPG key:](#1-add-dockers-official-gpg-key)
  - [2. Add the repository to Apt sources:](#2-add-the-repository-to-apt-sources)
  - [3. Install the Docker packages](#3-install-the-docker-packages)
  - [4. Verify](#4-verify)
- [A Shipping Analogy for Docker, Kubernetes, and Helm](#a-shipping-analogy-for-docker-kubernetes-and-helm)
  - [Docker: The Shipping Container](#docker-the-shipping-container)
  - [Kubernetes: The Port \& Crane System](#kubernetes-the-port--crane-system)
  - [Helm: The Shipping Manifest \& Blueprint](#helm-the-shipping-manifest--blueprint)
- [🧱 Main Docker Objects \& Entities](#-main-docker-objects--entities)
- [Docker Registries](#docker-registries)
  - [🧠 Choosing Tips](#-choosing-tips)
- [🐳 Docker Commands Cheat Sheet](#-docker-commands-cheat-sheet)
  - [Super commands](#super-commands)
  - [🧼 Docker Prune Command Comparison](#-docker-prune-command-comparison)
# How to install Docker on Ubuntu
## Reference:
- https://docs.docker.com/engine/install/ubuntu/

## 0. Uninstall all conflicting packages:
```shell
for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done
```
## 1. Add Docker's official GPG key:
```shell
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
```
## 2. Add the repository to Apt sources:
```shell
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
## 3. Install the Docker packages
```shell
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
## 4. Verify
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
# 🧱 Main Docker Objects & Entities
| Object            | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| **Images**        | Read-only templates for containers — define the app, OS, dependencies       |
| **Containers**    | Running instances of images — isolated, lightweight environments            |
| **Dockerfile**    | Script with instructions to build a custom image                            |
| **Volumes**       | Persistent data storage shared between host and containers                  |
| **Networks**      | Virtual communication bridges between containers and external services       |
| **Registries**    | Storage locations for images — e.g., Docker Hub, private registries         |
| **Layers**        | Each image is made up of stacked layers that improve caching and reuse      |
| **Context**       | The build directory passed to `docker build` — includes Dockerfile & assets |


# Docker Registries
| Registry                  | Type         | Highlights                                                  |
|---------------------------|--------------|-------------------------------------------------------------|
| **Docker Hub**            | Public/Private | Default registry, massive image library, CI/CD integration |
| **GitHub Container Registry** | Public/Private | Seamless with GitHub Actions, good for open-source projects |
| **GitLab Container Registry** | Private       | Built into GitLab CI/CD, great for internal pipelines       |
| **Amazon ECR**            | Private       | Deep AWS integration, IAM-based access control              |
| **Azure Container Registry (ACR)** | Private       | Geo-replication, RBAC, Helm chart support                   |
| **Google Artifact Registry** | Private       | Successor to GCR, supports multiple artifact types          |
| **Harbor**                | Private/Open Source | CNCF project, vulnerability scanning, RBAC, replication |
| **Quay.io / Red Hat Quay** | Private       | Enterprise-grade, geo-location support, BitTorrent delivery |
| **JFrog Artifactory**     | Private       | Universal repo manager, supports Docker + other formats     |
| **Sonatype Nexus Repository OSS** | Private       | Supports Docker, Maven, npm, and more                       |
## 🧠 Choosing Tips
- Public sharing? → Docker Hub (https://hub.docker.com/) or GitHub
- Enterprise security? → Harbor, Quay, or ECR
- CI/CD integration? → GitLab, GitHub, ACR
- Multi-artifact support? → JFrog or Nexus


# 🐳 Docker Commands Cheat Sheet
| Command                          | Purpose                                                   |
|----------------------------------|-----------------------------------------------------------|
| `docker run <image>`            | Create and start a container from an image               |
| `docker ps`                      | List running containers                                  |
| `docker ps -a`                  | List all containers (running + stopped)                  |
| `docker stop <container>`       | Gracefully stop a running container                      |
| `docker start <container>`      | Start a stopped container                                |
| `docker restart <container>`    | Restart a container                                      |
| `docker kill <container>`       | Forcefully stop a container                              |
| `docker rm <container>`         | Remove a container                                       |
| `docker exec -it <container> <cmd>` | Run a command inside a running container             |
| `docker logs <container>`       | View container logs                                      |
| `docker images`                 | List all local Docker images                             |
| `docker pull <image>`           | Download an image from Docker Hub                       |
| `docker build -t <name> .`      | Build an image from a Dockerfile                        |
| `docker rmi <image>`            | Remove an image                                          |
| `docker inspect <container>`    | View detailed info about a container/image               |
| `docker cp <src> <dest>`        | Copy files between host and container                    |
| `docker login`                  | Authenticate with Docker Hub                            |
| `docker push <image>`           | Upload an image to Docker Hub                           |
| `docker network ls`             | List Docker networks                                     |
| `docker volume ls`              | List Docker volumes                                      |
| `docker system prune`           | Clean up unused containers, images, volumes, networks    |
## Super commands
```shell
# List all docker objects
echo "================================================== CONTAINERS" && \
docker container ls --all && \
echo "================================================== IMAGES" && \
docker image ls --all && \
echo "================================================== NETWORKS" && \
docker network ls && \
echo "================================================== VOLUMES" && \
docker volume ls
```
```shell
# if there is at least 1 container running, the following command is best:
docker stop $(docker ps -q) && \
docker rm $(docker ps -aq) && \
docker rmi $(docker images -q) && \
docker network prune --force && \
docker volume prune --force && \
docker system prune --all --force
```
## 🧼 Docker Prune Command Comparison
| Command                               | Scope                    | What It Removes                                                                 |
|---------------------------------------|---------------------------|----------------------------------------------------------------------------------|
| `docker network prune --force`        | 🔌 Networks only           | All **unused Docker networks** not attached to containers                        |
| `docker system prune --all --force`   | 🌪️ Everything (aggressive) | - Stopped containers<br>- All unused images (not just dangling)<br>- Unused networks<br>- Unused volumes<br>- Build cache |
