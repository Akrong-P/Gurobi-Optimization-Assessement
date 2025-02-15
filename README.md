# Gurobi-Optimization-Assessement

# What are the differences between Docker and Kubernetes? Please give examples or applications for both tools. What other containerization tools do you know or are you familiar with?
Run a Gurobi Cluster Manager (version 11) in a Docker container. Provide a walkthrough of the steps you took; feel free to include specific commands used and/or any screenshots that demonstrate the process.  How can you add a new user to the Cluster Manager with the credentials CloudSupEng/password1234?
There is a communication issue between a Gurobi client machine and the Gurobi Compute Server. How can you figure out what might have caused the issue?
What are suitable Cloud machines on AWS or Azure (choose one service) for running Gurobi?
What makes Cloud machines preferable over running Gurobi on-premise? What are differences between Gurobi Cloud and a self-managed Compute Server or Cluster Manager?

====================================================================================================================================================================

# Solution

# Docker vs Kubernetes

## Docker

Docker is a platform used for developing, shipping, and running applications inside containers. Containers package an application and all its dependencies together, making the app portable and consistent across different environments.

### Key Features of Docker:
- **Lightweight**: Containers share the same OS kernel, making them much more lightweight than virtual machines.
- **Portability**: Once an application is containerized, it can be run anywhere that supports Docker (local machines, servers, or the cloud).
- **Isolation**: Docker ensures that applications run in their own isolated environments.

### Use Case Example:
Docker is often used to run microservices architectures, where each service is containerized separately and can be independently developed, tested, and deployed.

---

## Kubernetes

Kubernetes is an open-source orchestration tool used to manage containerized applications across clusters of machines. Kubernetes helps deploy, scale, and manage containerized applications in a seamless and automated way.

### Key Features:
- **Scaling**: Kubernetes allows you to scale your application containers up and down based on demand.
- **Self-healing**: It automatically replaces or restarts containers that fail.
- **Load Balancing**: Kubernetes can balance traffic across containers to ensure high availability.
- **Storage Orchestration**: It can automatically mount storage for containers as needed.

### Use Case Example:
Kubernetes is used for large-scale applications in cloud environments where many containers need to be managed. A typical use case might include managing microservices across multiple nodes.

---

## Key Differences

- **Docker**: Focused on containerization and provides the tools to build and run containers.
- **Kubernetes**: Provides orchestration of containers, helping manage them at scale in a cluster.

---

## Other Containerization Tools

- **Podman**: An alternative to Docker that allows users to run containers without a central daemon and supports rootless containers.
- **Docker Swarm**: A container orchestration tool provided by Docker, similar to Kubernetes but simpler, mainly used for smaller-scale orchestration.
- **OpenShift**: A Kubernetes-based container orchestration platform developed by Red Hat, offering additional enterprise features like enhanced security and automated workflows.

---

# Troubleshooting Gurobi Docker Containers

## Solution

1. **Search for Gurobi Docker Images**:
   Run the following command to find available Gurobi Docker images on Docker Hub:
   ```bash
   docker search gurobi
