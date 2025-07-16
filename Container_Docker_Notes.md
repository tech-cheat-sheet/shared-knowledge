- [How to install Docker on Ubuntu](#how-to-install-docker-on-ubuntu)
  - [Reference:](#reference)
  - [0. Uninstall all conflicting packages, if exist:](#0-uninstall-all-conflicting-packages-if-exist)
  - [1. Add Docker's official GPG key:](#1-add-dockers-official-gpg-key)
  - [2. Add the repository to Apt sources:](#2-add-the-repository-to-apt-sources)
  - [3. Install the Docker packages](#3-install-the-docker-packages)
  - [4. Verify](#4-verify)
- [A Shipping Analogy for Docker, Kubernetes, and Helm](#a-shipping-analogy-for-docker-kubernetes-and-helm)
  - [Docker: The Shipping Container](#docker-the-shipping-container)
  - [Kubernetes: The Port \& Crane System](#kubernetes-the-port--crane-system)
  - [Helm: The Shipping Manifest \& Blueprint](#helm-the-shipping-manifest--blueprint)
- [🧱 Main Docker Objects \& Entities](#-main-docker-objects--entities)
- [🐳 Docker: Main Components](#-docker-main-components)
  - [🧠 Docker Engine](#-docker-engine)
  - [📦 Docker Images](#-docker-images)
  - [🚀 Docker Containers](#-docker-containers)
  - [🗂️ Docker Registries](#️-docker-registries)
  - [🌐 Docker Networking](#-docker-networking)
    - [Network Drivers:](#network-drivers)
    - [💾 Docker Volumes](#-docker-volumes)
  - [🧩 Advanced Components](#-advanced-components)
  - [🧮 Container Runtime vs Container Engine Comparison](#-container-runtime-vs-container-engine-comparison)
  - [🧮 Containerd vs CRI-O Comparison Table](#-containerd-vs-cri-o-comparison-table)
    - [🔍 Summary:](#-summary)
  - [🧩 Container Technology Stack Overview](#-container-technology-stack-overview)
  - [🔍 Summary](#-summary-1)
  - [🧮 Container vs Virtual Machine Comparison](#-container-vs-virtual-machine-comparison)
- [Docker Registries](#docker-registries)
  - [🧠 Choosing Tips](#-choosing-tips)
- [🐳 Docker Commands Cheat Sheet](#-docker-commands-cheat-sheet)
  - [Super commands - Start from a clean state](#super-commands---start-from-a-clean-state)
  - [🧼 Docker Prune Command Comparison](#-docker-prune-command-comparison)
- [🧩 Container Standards \& Interfaces Comparison](#-container-standards--interfaces-comparison)
# How to install Docker on Ubuntu
## Reference:
- https://docs.docker.com/engine/install/ubuntu/

## 0. Uninstall all conflicting packages, if exist:
```shell
for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done
```
## 1. Add Docker's official GPG key:
```shell
sudo apt-get update --yes && \
sudo apt-get install --yes ca-certificates curl && \
sudo install -m 0755 -d /etc/apt/keyrings && \
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc && \
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
sudo apt-get install --yes docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
## 4. Verify
```shell
which docker

docker --version

sudo docker run hello-world

## 5. Run 'docker' commands without 'sudo'
# https://docs.docker.com/engine/install/linux-postinstall/
whoami
groups
getent group | grep -i docker
sudo groupadd docker
sudo usermod -aG docker $USER && newgrp docker
whoami
groups
# 🔍 Why You Lose It After 'exit'
# When you run 'newgrp docker', you're in a temporary subshell with updated group membership.
# When you type 'exit', you leave that subshell and return to your original shell session, which was started before your group membership changed.
# That original shell doesn’t know about the new group membership yet.
# To make the group membership apply system-wide:
# 1. Log out completely from your user session (not just the terminal).
# 2. Log back in—this refreshes your group memberships.
# 3. Run groups again, and you’ll see docker included.
exit
sudo reboot
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


# 🐳 Docker: Main Components
## 🧠 Docker Engine
The heart of Docker's architecture.
- Docker Daemon (dockerd): Background service managing containers.
- REST API: Interface for remote management of Docker features.
- Docker CLI: Command-line tool (docker) used to interact with Docker.
## 📦 Docker Images
Templates used to create containers.
- Built from a Dockerfile.
- Can be pulled from Docker Hub or built locally.
- Immutable and reusable across environments.
## 🚀 Docker Containers
Running instances of images.
- Lightweight and isolated from the host OS.
- Easily managed using CLI commands.
- Ideal for deploying services and apps consistently.
## 🗂️ Docker Registries
Storage and distribution hubs for images.
- Docker Hub: Default public registry.
- Private Registries: Custom repositories for internal use.
## 🌐 Docker Networking
Enables communication between containers and the outside world.
### Network Drivers:
- Bridge – Default, connects containers on a host.
- Host – Shares host’s networking stack.
- Overlay – Connects containers across multiple hosts.
- None – Disables all networking.
- Macvlan – Assigns a MAC address to containers for direct access.
### 💾 Docker Volumes
Persistent data storage.
- Remains intact across container restarts or deletions.
- Used for sharing data between containers.
## 🧩 Advanced Components
- Docker Compose: Defines multi-container apps using a docker-compose.yml file.
- Docker Swarm: Built-in orchestration tool for clustering and managing distributed containers.
## 🧮 Container Runtime vs Container Engine Comparison
| **Aspect**               | **Container Runtime**                                      | **Container Engine**                                      |
|--------------------------|------------------------------------------------------------|-----------------------------------------------------------|
| **Purpose**              | Executes containers by interfacing with OS kernel features | Manages full container lifecycle including image handling |
| **Scope**                | Low-level operations (start, stop, isolate containers)      | High-level orchestration, image building, CLI/API support |
| **Examples**             | `runc`, `crun`, `runhcs`                                    | `Docker Engine`, `Podman`, `CRI-O`, `containerd`          |
| **User Interaction**     | Typically not used directly by developers                   | Provides CLI/API for developers and operators             |
| **Image Management**     | No image building or pulling capabilities                   | Pulls, builds, and manages container images               |
| **Networking & Storage** | Relies on engine or external plugins                        | May include built-in networking and storage features      |
| **Integration**          | Used by engines and orchestrators like Kubernetes           | Interfaces with runtimes and orchestrators                |
| **Standardization**      | Follows OCI Runtime Specification                           | Often follows OCI Image Specification                     |
| **Complexity Level**     | Lightweight and minimal                                     | More feature-rich and complex                            |
| **Use Case**             | Kernel-level container execution                            | Full container lifecycle management                       |

Think of the runtime as the engine block of a car—it powers the container. The container engine is the dashboard and controls—it lets you drive, steer, and manage the whole experience.


## 🧮 Containerd vs CRI-O Comparison Table
| **Aspect**               | **containerd**                                             | **CRI-O**                                                  |
|--------------------------|------------------------------------------------------------|-------------------------------------------------------------|
| **Purpose**              | General-purpose container runtime                          | Lightweight runtime focused solely on Kubernetes             |
| **Origin**               | Developed by Docker, now part of CNCF                      | Created by Red Hat, maintained by Kubernetes community       |
| **CRI Compatibility**    | Requires CRI plugin (`cri-containerd`)                     | Built specifically to implement Kubernetes CRI               |
| **OCI Compliance**       | Fully OCI-compliant (images and runtime)                   | Fully OCI-compliant                                          |
| **Architecture**         | Daemon-based, manages full container lifecycle             | Daemon-less, minimal components tailored for Kubernetes      |
| **Image Handling**       | Pulls, stores, and manages container images                | Uses `containers/image` library for image management         |
| **Security Features**    | Supports gVisor, Kata Containers, seccomp, AppArmor        | Emphasizes SELinux, AppArmor, and minimal attack surface     |
| **Resource Footprint**   | Moderate                                                   | Very lightweight                                             |
| **Popular Use Cases**    | Kubernetes, Docker replacement, CI/CD pipelines            | Kubernetes-native clusters, OpenShift                        |
| **Community & Ecosystem**| Large CNCF ecosystem, widely adopted                       | Smaller but growing Kubernetes-focused community             |
| **Extensibility**        | Highly extensible via plugins and APIs                     | Focused on Kubernetes extensibility                          |
| **Logging & Monitoring** | Integrated with Kubernetes logging                         | Uses `conmon` for container monitoring and logging           |
| **Networking**           | Relies on CNI plugins                                      | Relies on CNI plugins                                        |
| **Storage Support**      | Integrates with CSI plugins                                | Integrates with CSI plugins                                  |

### 🔍 Summary:
- containerd is versatile and widely used beyond Kubernetes, making it a solid choice for general container management.
- CRI-O is purpose-built for Kubernetes, offering a leaner, more secure runtime with minimal overhead.


## 🧩 Container Technology Stack Overview
This image outlines how different container technologies and runtimes interconnect, especially in Kubernetes environments:
```shell
Kubernetes interfaces with the CRI to talks to Containerd
or
Kubernetes interfaces with the CRI to talks to CRI-O

Containerd talks to RUNC (OCI)
CRI-O talks to RUNC (OCI)

RUNC enables 'running container'
```
| **Layer**              | **Components & Relationships**                                                                                                                                   |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Container Engines**  | - **Docker** and **Podman**: User-facing tools for building and managing containers.                                                                            |
| **Runtime Interfaces** | - **CRI-O** and **Containerd**: Act as bridges between Kubernetes and low-level runtimes.<br>• CRI-O works well with Podman and Docker.<br>• Containerd connects directly with Kubernetes. |
| **Runtime Spec (OCI)** | - **runc**: The low-level container runtime used by CRI-O and Containerd to start and stop containers following the Open Container Initiative (OCI) spec.        |
| **Orchestration**      | - **Kubernetes**: Manages containers at scale; communicates with CRI-O or Containerd using the **Container Runtime Interface (CRI)**.                           |
| **Output**             | - **Running Containers**: The result of orchestration and runtime execution across the system.                                                                  |
## 🔍 Summary
- Podman/Docker help define and manage containers.
- CRI-O/Containerd translate Kubernetes commands into container operations.
- runc handles the low-level execution based on standardized specs.
- Kubernetes ties it all together—it's the master conductor.
- The final product: containers running seamlessly across infrastructure.


## 🧮 Container vs Virtual Machine Comparison
| **Aspect**               | **Container**                                              | **Virtual Machine (VM)**                                  |
|--------------------------|------------------------------------------------------------|-----------------------------------------------------------|
| **Virtualization Level** | OS-level virtualization                                    | Hardware-level virtualization                             |
| **Isolation**            | Lightweight isolation; shares host OS kernel              | Strong isolation; includes its own OS and kernel          |
| **Startup Time**         | Fast (seconds)                                             | Slower (minutes)                                          |
| **Resource Usage**       | Low (shares OS resources)                                  | High (dedicated OS per VM)                                |
| **Size**                 | Small (typically MBs)                                      | Large (typically GBs)                                     |
| **Portability**          | Highly portable across environments                        | Less portable; OS dependencies can vary                   |
| **Security**             | Lower isolation; shared kernel can be a risk               | Higher isolation; better for sensitive workloads          |
| **Use Cases**            | Microservices, CI/CD pipelines, cloud-native apps          | Legacy apps, multi-OS environments, strong security needs |
| **Management Tools**     | Docker, Podman, Kubernetes                                 | VMware, Hyper-V, VirtualBox                               |
| **Performance Overhead** | Minimal                                                    | Higher due to full OS emulation                           |

🧠 Think of containers as lightweight, agile runners, and VMs as fully equipped armored vehicles—each has its place depending on the terrain you're navigating.


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
## Super commands - Start from a clean state
```shell
## List all docker objects
echo "================================================== CONTAINERS" && \
docker container ls --all && \
echo "================================================== IMAGES" && \
docker image ls --all && \
echo "================================================== NETWORKS" && \
docker network ls && \
echo "================================================== VOLUMES" && \
docker volume ls
# # if there is at least 1 container running, the following command is best:
echo "================================================== Stopping all running containers" && \
docker stop $(docker ps -q) && \
echo "================================================== Removing all containers" && \
docker rm $(docker ps -aq) && \
echo "================================================== Removing all images" && \
docker rmi $(docker images -q) && \
echo "================================================== Removing all networks" && \
docker network prune --force && \
echo "================================================== Removing all volumes" && \
docker volume prune --force && \
echo "================================================== Docker system cleanup" && \
docker system prune --all --force
```
## 🧼 Docker Prune Command Comparison
| Command                               | Scope                    | What It Removes                                                                 |
|---------------------------------------|---------------------------|----------------------------------------------------------------------------------|
| `docker network prune --force`        | 🔌 Networks only           | All **unused Docker networks** not attached to containers                        |
| `docker system prune --all --force`   | 🌪️ Everything (aggressive) | - Stopped containers<br>- All unused images (not just dangling)<br>- Unused networks<br>- Unused volumes<br>- Build cache |


# 🧩 Container Standards & Interfaces Comparison
| **Aspect**                | **Open Container Initiative (OCI)**                          | **Container Network Interface (CNI)**                     | **Container Runtime Interface (CRI)**                     | **Container Storage Interface (CSI)**                     | **Service Mesh Interface (SMI)**                          |
|--------------------------|---------------------------------------------------------------|-----------------------------------------------------------|-----------------------------------------------------------|-----------------------------------------------------------|-----------------------------------------------------------|
| **Purpose**              | Define open standards for container images and runtimes       | Standardize container networking across platforms         | Enable Kubernetes to interact with container runtimes     | Standardize volume/storage management in Kubernetes       | Provide a common interface for service mesh features      |
| **Scope**                | Industry-wide container format and runtime specs              | Networking plugins for container orchestration systems    | Kubernetes-specific runtime abstraction                   | Kubernetes-specific storage abstraction                   | Kubernetes-focused service mesh abstraction               |
| **Key Components**       | `image-spec`, `runtime-spec`, `distribution-spec`             | IP address management, routing, DNS                       | `RuntimeService`, `ImageService` gRPC APIs                | Volume provisioning, attach/detach, mount/unmount         | Traffic policies, telemetry, access control               |
| **Primary Use Case**     | Ensuring container portability and interoperability           | Plug-and-play networking for containers                   | Decouple Kubernetes from specific runtimes (e.g. Docker)  | Enable dynamic storage provisioning in clusters           | Unified service mesh behavior across implementations      |
| **Popular Implementations** | Docker, containerd, runc                                     | Calico, Flannel, Cilium                                  | containerd, CRI-O                                         | Rook, OpenEBS, Portworx                                   | Istio, Linkerd, Consul (via SMI adapter)                  |
| **Governance**           | Maintained by the Linux Foundation                            | CNCF project                                               | Kubernetes project                                        | Kubernetes project                                        | CNCF project                                               |
| **Interoperability Goal**| Cross-platform container compatibility                        | Modular networking stack                                  | Runtime flexibility in Kubernetes                         | Storage vendor neutrality                                 | Mesh-agnostic service mesh tooling                        |

These interfaces and standards are like the plumbing and wiring behind the scenes of modern container orchestration. They don’t always get the spotlight, but they’re what make the magic of Kubernetes and cloud-native apps possible.
