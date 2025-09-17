# CI/CD Pipeline with Kubernetes Deployment

## 📌 Overview
This project demonstrates a CI/CD pipeline for a simple microservice application.
- Code commit → GitHub Actions builds + pushes Docker image to DockerHub
- Deploys app to Kubernetes (Minikube/Kind cluster)
- Service exposed via NodePort

## ⚙️ Tech Stack
- Python (Flask app)
- Docker
- GitHub Actions
- Kubernetes (Minikube)

## 🚀 Setup Instructions

### 1. Clone Repo
```bash
git clone https://github.com/<your-username>/ci-cd-k8s-demo.git
cd ci-cd-k8s-demo
```

### 2. Setup DockerHub Secrets in GitHub
Go to `Repo → Settings → Secrets → Actions` and add:
- `DOCKER_USERNAME`
- `DOCKER_PASSWORD`

### 3. Start Minikube
```bash
minikube start
```

### 4. Trigger CI/CD
Push code → GitHub Actions runs → Docker image pushed → Deployment applied.

### 5. Access Service
```bash
minikube service demo-service
```
Open browser → `Hello from CI/CD + Kubernetes Demo!`

---

## ✅ Demo Checklist
1. Show code commit triggers pipeline
2. Show pipeline steps (build, push, deploy)
3. Show Kubernetes pods running
4. Show app in browser
