# CI/CD with Docker and Kubernetes

##  Overview

This repository demonstrates a hands-on **DevOps CI/CD pipeline** using **Docker** for containerization and **Kubernetes** for deployment.  
The project simulates a realistic workflow where application code is built into a container image, pushed to a registry, and deployed to a Kubernetes cluster.

This project is part of self-directed DevOps training focused on building practical, production-relevant skills.

---

## Project Structure


├── app/ # Application source code

├── Dockerfile # Docker image build definition

├── k8s/ # Kubernetes manifests

│ ├── deployment.yaml # Kubernetes Deployment

│ └── service.yaml # Kubernetes Service

├── deployment.yaml # Deployment manifest (root)

├── service.yaml # Service manifest (root)

└── README.md # Project documentation

---

## Workflow Overview

1. Application source code is packaged into a Docker image using a Dockerfile.
2. The container image can be built and pushed to a container registry.
3. Kubernetes manifests define how the application is deployed and exposed.
4. The application runs in a Kubernetes cluster using declarative configuration.
5. Git & GitHub are used to version and manage the workflow.

This reflects a simplified but realistic CI/CD-to-Kubernetes deployment process.

---

## Prerequisites

- Docker
- Kubernetes cluster (Minikube, kind, or cloud-managed)
- kubectl configured for cluster access
- Git

---

## Usage

### Clone the repository
```bash
git clone https://github.com/Chisney25/ci-cd-docker-kubernetes.git
cd ci-cd-docker-kubernetes
```
Build the Docker image
```bash
docker build -t ci-cd-app:latest .
```
Deploy to Kubernetes
```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```
Verify deployment
```bash
kubectl get pods
kubectl get services
```

---

## Skills Demonstrated
- Docker containerization
- Kubernetes deployments and services
- CI/CD workflow fundamentals
- Infrastructure as code (YAML)
- Linux and CLI usage
- Git & GitHub version control

---

## Future Improvements
- Add GitHub Actions CI pipeline
- Automate image build and push
- Trigger Kubernetes deployment from CI
- Add monitoring and logging

---

## Links
- GitHub: https://github.com/Chisney25
- LinkedIn: https://www.linkedin.com/in/chisommiracle

---