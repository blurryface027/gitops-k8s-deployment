# GitOps-Based Kubernetes Deployment using ArgoCD and Helm

This project demonstrates a GitOps-based Kubernetes deployment where GitHub acts as the single source of truth. Application deployment, scaling, self-healing, and rollback are fully automated using ArgoCD and Helm without manual kubectl intervention.

---

## Project Overview

Modern DevOps teams use GitOps to manage Kubernetes deployments in a reliable and auditable way. In this project, all Kubernetes configuration is stored in GitHub, and ArgoCD continuously synchronizes the cluster state with the repository.

---

## Architecture

Developer → GitHub Repository → ArgoCD → Kubernetes Cluster → Running Application

---

## Technology Stack

- GitHub – Source of Truth  
- Kubernetes – Container orchestration  
- Helm – Kubernetes configuration management  
- ArgoCD – GitOps continuous delivery  
- Docker – Containerized application (Nginx)  
- Linux – Development environment  

---

## Features

- GitOps-based Kubernetes deployment
- Automated deployment using ArgoCD
- Helm-based configuration management
- Git-driven application scaling
- Git-based rollback to last stable version
- Kubernetes self-healing
- No manual kubectl apply usage

---

## Repository Structure

gitops-k8s-deployment/
├── nginx-app/
│   ├── Chart.yaml
│   ├── values.yaml
│   └── templates/
│       ├── deployment.yaml
│       └── service.yaml
└── README.md

---

## How It Works

1. Application configuration is defined using Helm charts and stored in GitHub.
2. ArgoCD continuously watches the repository.
3. Any change pushed to GitHub is automatically applied to the Kubernetes cluster.
4. Kubernetes ensures the desired state through self-healing and scaling.

---

## Scaling (GitOps Way)

Update replica count in values.yaml:

replicaCount: 4

Commit and push the change. ArgoCD automatically scales the application.

---

## Rollback Strategy

If a faulty change is deployed:
- Revert the Git commit
- ArgoCD automatically restores the previous stable state

---

## Key Concepts Demonstrated

- GitOps workflow
- Git as single source of truth
- Continuous reconciliation
- Kubernetes scaling and self-healing
- Helm templating
- Git-based rollback

---

## Author

Krishna Sharma  
GitHub: https://github.com/blurryface027

---

## License

This project is for learning and demonstration purposes.
