# 🚀 Kubernetes Overview

**Kubernetes (K8s)** is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications. Originally developed by **Google**, it is now managed by the **Cloud Native Computing Foundation (CNCF)**. Kubernetes helps you manage clusters of containers at scale, making it an essential tool for modern application management.

---

## 🔧 What Problems Does Kubernetes Solve?

- **Manual Deployment**: Automates configuration, scaling, and updates.
- **Scalability**: Automatically scales applications based on real-time traffic.
- **Fault Tolerance**: Ensures high availability by restarting failed containers.
- **Service Discovery**: Manages internal load balancing and service discovery.
- **Resource Optimization**: Dynamically allocates resources based on usage.
- **Version Management**: Simplifies complex application updates and rollbacks.

---

## ✨ Key Features of Kubernetes

- **Automated Rollouts & Rollbacks**: Manage app updates seamlessly and revert in case of issues.
- **Self-Healing**: Automatically restarts and replaces failed containers.
- **Load Balancing & Service Discovery**: Distributes network traffic and manages container discovery.
- **Horizontal Scaling**: Automatically adjusts container count based on demand.
- **Storage Orchestration**: Abstracts underlying storage systems and manages persistent storage.
- **Infrastructure Abstraction**: Run containers consistently across any infrastructure (cloud or on-prem).

---

## 🛠️ Main Kubernetes Components

### 🔹 Node & Pod
- **Node**: Worker machine (physical or virtual) where Kubernetes applications run.
- **Pod**: Smallest deployable unit that encapsulates one or more containers.

### 🔹 Service & Ingress
- **Service**: Provides a stable endpoint for accessing a set of pods.
- **Ingress**: Manages external access (e.g., HTTP/HTTPS) to services within the cluster.

### 🔹 ConfigMap & Secret
- **ConfigMap**: Stores non-sensitive configuration data.
- **Secret**: Securely stores sensitive data such as passwords and API keys.

### 🔹 Volumes
- **Volume**: Provides persistent storage that can be shared between containers and survive restarts.

### 🔹 Deployment & StatefulSet
- **Deployment**: Manages stateless applications, handles scaling and rolling updates.
- **StatefulSet**: Manages stateful applications, ensuring persistence and maintaining unique identities for pods.

---

## 🏗️ Kubernetes Architecture

Kubernetes architecture consists of **master nodes** and **worker nodes**. The **control plane** (master nodes) manages the cluster, while the **worker nodes** run application workloads.

### **Master Node Components:**

| Component               | Description                                                                                                                   |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| **API Server**           | Exposes the Kubernetes API, acting as the front-end for the control plane.                                                     |
| **Scheduler**            | Assigns newly created pods to nodes based on resource availability and constraints.                                            |
| **Controller Manager**   | Monitors the cluster state and ensures it matches the desired state. Manages nodes, pods, and replicas.                        |
| **etcd**                 | Distributed key-value store that stores all Kubernetes cluster data and configuration. It's the brain of the Kubernetes cluster.|

### **Worker Node Components:**

| Component               | Description                                                                                                                    |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **Kubelet**              | Agent that runs on each node, ensuring containers are running as expected.                                                     |
| **Kube-proxy**           | Maintains networking rules on nodes and facilitates communication between containers.                                          |
| **Container Runtime**    | Software responsible for running containers (e.g., Docker, containerd).                                                        |

---
