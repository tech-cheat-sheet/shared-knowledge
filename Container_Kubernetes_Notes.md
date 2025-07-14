- [Kubernetes (K8S)](#kubernetes-k8s)
- [📊 Container Orchestration Comparison Table](#-container-orchestration-comparison-table)
  - [🚀 Core Concepts](#-core-concepts)
  - [⚙️ Kubernetes Capabilities](#️-kubernetes-capabilities)
  - [🧠 Philosophy](#-philosophy)
  - [🌍 Real-World Use Cases](#-real-world-use-cases)
- [Ubuntu and Kubernetes](#ubuntu-and-kubernetes)
  - [🧪 Option 1: Minikube (Best for Beginners)](#-option-1-minikube-best-for-beginners)
  - [🧰 Option 2: MicroK8s (Canonical’s Lightweight Kubernetes)](#-option-2-microk8s-canonicals-lightweight-kubernetes)
- [Minikube](#minikube)
  - [🚀 Minikube Main Commands Cheat Sheet](#-minikube-main-commands-cheat-sheet)
  - [Super command](#super-command)
- [🧰 kubectl Main Commands Cheat Sheet](#-kubectl-main-commands-cheat-sheet)
# Kubernetes (K8S)
Kubernetes (often abbreviated as K8s) is an open-source platform designed to automate the deployment, scaling, and management of containerized applications2. Think of it as the operating system for your data center — orchestrating containers like a conductor leading an orchestra.
# 📊 Container Orchestration Comparison Table
| Feature                      | Docker Compose                         | Docker Swarm                          | Kubernetes                              |
|-----------------------------|----------------------------------------|---------------------------------------|------------------------------------------|
| 🚀 Purpose                   | Local multi-container development      | Basic container orchestration         | Advanced orchestration & scaling         |
| 🛠 Complexity                | Low                                     | Moderate                              | High                                      |
| 📦 Setup Time               | Minutes                                 | Few minutes                           | Hours (or use managed services)          |
| 🧩 Configuration Language   | YAML                                    | YAML + CLI                            | YAML + kubectl + many config types       |
| 🔁 Scaling Support          | Manual scale                            | Built-in scaling                      | Autoscaling, rolling updates             |
| 🧪 Health Checks            | Basic                                   | Supported                             | Robust, customizable                     |
| 🔌 Networking               | Simple bridge network                   | Overlay networks                      | Advanced networking model                |
| 🏗 Service Discovery        | Limited                                 | Built-in                              | DNS-based, automatic                     |
| 📦 Volume Management        | Simple                                  | Supported                             | Extensive with persistent volumes        |
| 🌐 Cloud Native Support     | Minimal                                 | Limited                               | Strong (cloud providers love it)         |
| 🧑‍🤝‍🧑 Community & Ecosystem | Small                                   | Niche                                  | Large, thriving ecosystem                |
| 📦 Use Case Example         | Dev/testing multi-service apps          | Small scale deployments               | Microservices at scale                   |
## 🚀 Core Concepts
- Containers: Lightweight, portable units that package code and dependencies.
- Pods: The smallest deployable unit in Kubernetes, often wrapping one or more containers.
- Nodes: Machines (physical or virtual) that run your workloads.
- Cluster: A group of nodes managed together.
- Control Plane: The brain of Kubernetes, scheduling and managing workloads.
- Kubelet & Kube-proxy: Agents on nodes that ensure containers run and communicate properly.
## ⚙️ Kubernetes Capabilities
| Capability             | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| **Deployment Automation** | Launches and manages containers across clusters                           |
| **Self-Healing**          | Restarts failed containers, replaces unhealthy ones                       |
| **Scaling**               | Automatically adjusts resources based on demand                           |
| **Load Balancing**        | Distributes traffic across containers for stability                       |
| **Rollouts & Rollbacks**  | Updates apps with zero downtime and reverts if needed                     |
| **Storage Orchestration** | Mounts local or cloud storage as needed                                   |
| **Secret Management**     | Securely stores sensitive data like passwords and tokens                  |
## 🧠 Philosophy
Kubernetes uses a declarative model: you define your desired state (e.g., 5 replicas of an app), and Kubernetes continuously works to make reality match that state.
## 🌍 Real-World Use Cases
- E-commerce platforms handling millions of users
- Media streaming with global content delivery
- Financial services requiring secure, scalable infrastructure
- Healthcare systems managing patient data and analytics
# Ubuntu and Kubernetes
## 🧪 Option 1: Minikube (Best for Beginners)
```shell
# Install dependencies
sudo apt update

# Install Minikube
curl -LO https://github.com/kubernetes/minikube/releases/latest/download/minikube-linux-amd64

sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64

# 🛠️ Fix: Enable Docker Driver
docker --version
sudo usermod -aG docker $USER
newgrp docker

# Start your cluster
minikube start --driver=docker

# Minikube internal tool
minikube kubectl -- get pods -A

# Use kubectl to interact
sudo apt update
sudo apt install snapd -y
sudo snap install kubectl --classic
# ✅ Pros: Fast, simple, auto-updates 
# ⚠️ Cons: May not always be the latest version
kubectl get pods --all-namespaces
```
Sources:
- https://minikube.sigs.k8s.io/docs/start

✅ Pros: Easy setup, low resource usage

⚠️ Cons: Not production-grade, limited to one node
## 🧰 Option 2: MicroK8s (Canonical’s Lightweight Kubernetes)
```shell
# Install MicroK8s
sudo snap install microk8s --classic

# Add your user to the MicroK8s group
sudo usermod -a -G microk8s $USER
newgrp microk8s

# Enable common add-ons
microk8s enable dns dashboard storage

# Check cluster status
microk8s status --wait-ready
```
✅ Pros: Fast, modular, supports multi-node

⚠️ Cons: Snap-based, may need extra config for networking
# Minikube
## 🚀 Minikube Main Commands Cheat Sheet
| Command                            | Purpose                                                   |
|------------------------------------|-----------------------------------------------------------|
| `minikube start`                   | Launches a local Kubernetes cluster                       |
| `minikube stop`                    | Stops the running cluster                                 |
| `minikube delete`                 | Deletes the cluster and its configuration                 |
| `minikube status`                  | Displays current cluster status                           |
| `minikube dashboard`              | Opens the Kubernetes dashboard in your browser            |
| `minikube addons list`            | Lists available add-ons                                   |
| `minikube addons enable <name>`   | Enables a specific add-on                                 |
| `minikube addons disable <name>`  | Disables a specific add-on                                |
| `minikube service <svc-name>`     | Opens a service in your browser                           |
| `minikube ip`                      | Shows the cluster’s IP address                            |
| `minikube logs`                    | Displays cluster logs for troubleshooting                 |
| `minikube config view`            | Shows current configuration settings                      |
| `minikube update-check`           | Checks for Minikube updates                               |
| `minikube ssh`                     | SSH into the Minikube VM/container                        |
## Super command
```shell
minikube start --driver=docker --cpus=4 --memory=8192 --disk-size=10g
# Check cpu count with 'lscpu'
# Check memory with 'free -h'
# Check disk space with 'df -h'
```

# 🧰 kubectl Main Commands Cheat Sheet
| Command                            | Purpose                                                   |
|------------------------------------|-----------------------------------------------------------|
| `kubectl get <resource>`           | List resources (pods, services, deployments, etc.)        |
| `kubectl describe <resource>`      | Show detailed info about a resource                       |
| `kubectl apply -f <file>`          | Create or update resources from a YAML/JSON file          |
| `kubectl create <resource>`        | Create a resource manually                                |
| `kubectl delete <resource>`        | Delete a resource                                         |
| `kubectl edit <resource>`          | Edit a resource in your default editor                    |
| `kubectl logs <pod>`               | View logs from a pod                                      |
| `kubectl exec <pod> -- <cmd>`      | Run a command inside a pod                                |
| `kubectl port-forward <pod/service>`| Forward local port to pod/service                         |
| `kubectl scale <resource>`         | Scale a deployment or replicaset                          |
| `kubectl rollout <subcommand>`     | Manage deployment rollouts (status, undo, restart)        |
| `kubectl top <resource>`           | View resource usage (CPU/memory)                          |
| `kubectl config <subcommand>`      | Manage kubeconfig contexts and clusters                   |
| `kubectl get all`                  | List all resources in the current namespace               |
