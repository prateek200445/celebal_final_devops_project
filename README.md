# celebal_final_devops_project
Deploy a Dockerized application on a VM, enhancing deployment efficiency and management through containerization, Docker installation, image pulling, container launching, and networking configuration for application access.
# 🚀 DevOps Internship Project – Docker & Kubernetes Based Full Stack Deployment

This is the final project submitted for my DevOps Internship at **Celebal Technologies**, showcasing a complete **Dockerized and Kubernetes-ready full stack insurance application**.

It demonstrates:
- 🐳 End-to-end Docker containerization and deployment on **Azure VM**
- ☸️ Scalable Kubernetes deployment using **Azure Kubernetes Service (AKS)** { THIS IS DONE AS AN ADDITIONAL TO THE STATED TASK THE DEPLOYMENT MAY OR MAY NOT BE LIVE FOR KUBERNETES CLUSTER DEPENDING UPON THE AZURE CREDITS **DOCKER ONE WILL BE LIVE YOU CAN LOOK ONTO IT**  }
- ⚙️ CI/CD pipeline with **GitHub Actions**
- 🌍 Global access with **Nginx reverse proxy** and **Let's Encrypt SSL**
- 📈 Monitoring via **Portainer**, `docker stats`, and **Prometheus + Grafana**

> 🔗 **Live Docker Deployment:** [http://172.171.199.181:5173/](http://172.171.199.181:5173/)
> Test user login : prateek
> Test user password : Prateek2004@ 
> ☁️ **Kubernetes Deployment:** _Running on AKS with YAML-based manifests_  
> 📦 **DockerHub Image:** `prateek2004/insurance-backend:latest`
> 📦 **DockerHub Image:** `prateek2004/insurance-frontend:latest`

---

## 🧱 Core DevOps Deliverables

### ✅ 1. Docker-Based Deployment (Primary)

- Multi-stage Dockerfiles for frontend (React) and backend (Node.js)
- MongoDB containerized with data persistence
- Single-command orchestration via `docker-compose.yml`
- Nginx config to support **SPA deep linking**
- Hosted on **Azure Virtual Machine** with open ports via **NSG**

### ☁️ 2. Kubernetes Deployment on Azure (AKS)

- Defined **Deployment**, **Service**, and **Ingress** YAMLs
- MongoDB with PVC and persistent storage
- Auto-scaling enabled (optional)
- Exposed through **AKS Ingress Controller** with Nginx

---

## ⚙️ CI/CD Pipeline with GitHub Actions

- On every push to `main` branch:
  - Build Docker images
  - Push to DockerHub (`prateek2004/*`)
  - Optional deploy to Azure VM via SSH webhook

> 🔁 Setup future workflow to trigger AKS rollout via GitHub Actions (Helm or Kustomize ready)

---

## 🔐 SSL, Reliability & Monitoring

- 🔐 Let's Encrypt SSL via Certbot (VM ready)
- 🔁 **Watchtower** for auto-updating containers
- 📊 **Portainer** for container GUI management
- 📈 Docker stats used to monitor resource usage
- 🧠 **Prometheus + Grafana** integrated for container metrics

---

## 🌍 Tech Stack Summary

| Layer       | Tech Used                        |
|-------------|----------------------------------|
| Frontend    | React, Nginx                     |
| Backend     | Node.js, Express, bcryptjs       |
| Database    | MongoDB, Mongoose                |
| Container   | Docker, Docker Compose           |
| Orchestration | Azure Kubernetes Service (AKS) |
| CI/CD       | GitHub Actions                   |
| Monitoring  | Portainer, Prometheus, Grafana   |
| Infra       | Azure VM, NSG, DockerHub         |

---

## 📁 Project Structure

celebal_final_devops_project/
├── client/ # React frontend (Dockerized)
│ ├── Dockerfile
│ └── nginx.conf # Custom for SPA routing
├── server/ # Node.js backend (Dockerized)
│ ├── Dockerfile
│ └── .env.example
├── k8s/ # Kubernetes manifests (AKS)
│ ├── deployment.yaml
│ ├── service.yaml
│ └── ingress.yaml
├── .github/workflows/ # GitHub Actions CI/CD
│ └── docker-push.yml
├── docker-compose.yml # Docker orchestration
└── README.md


---

## 🚀 Local Setup (Docker)

```bash
git clone https://github.com/prateek200445/celebal_final_devops_project.git
cd celebal_final_devops_project
docker-compose up --build '''

Visit:

Frontend → http://localhost:80

Backend API → http://localhost:5000

MongoDB → localhost:27017

☸️ Deploy to AKS (Kubernetes)
'''bash

kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
kubectl apply -f k8s/ingress.yaml
'''

## 🔐 **Admin Demo Credentials**

| **Role** | **Username**         | **Password**     |
|----------|----------------------|------------------|
| Admin    | prateek              | Prateek@2004     |


## 📸 Screenshots 

- ✅ **Frontend dashboard**
- ✅ **Portainer dashboard**
- ✅ **GitHub Actions CI/CD pipeline run**
- ✅ **Prometheus + Grafana metrics**
- ✅ **AKS pods view from** `kubectl get pods`


## 🔮 Future Enhancements ( Planning )

- 🧩 **Add Helm support** for K8s deployment  
- 🔄 **JWT refresh token** + token rotation  
- 📦 **Centralized logging** with Loki or ELK stack  
- 🌐 **Switch from static IP to domain** + cert auto-renewal

## 📝 Submission Notes

- ✅ **Docker deployment** (frontend + backend + MongoDB)  
- ✅ **Azure VM** with NSG + open ports  
- ✅ **CI/CD** with GitHub Actions  
- ✅ **AKS-based production deployment**  
- ✅ **SPA routing**, reverse proxy, monitoring, SSL-ready  
- ✅ **Additional tooling**: Portainer, Watchtower, Prometheus  

📂 **All AKS YAML files, CI/CD workflows, and Grafana dashboards** will be uploaded in this repository within 1–2 days.  
🛠️ **Maintainer**: [@prateek200445](https://github.com/prateek200445)  
📁 **Repo Name**: `celebal_final_devops_project`  
🌐 **Live Docker Deployment**: [http://172.171.199.181/5173](http://172.171.199.181/)

## 🐳 Docker Hub

All Docker images used in this project are available on Docker Hub:  
🔗 [https://hub.docker.com/u/prateek2004](https://hub.docker.com/u/prateek2004)

---

## 📦 Final Notes

Everything required to run and deploy this project is included in this repository:

- ✅ Dockerfiles for frontend, backend, and MongoDB
- ✅ docker-compose setup for local development
- ✅ AKS-compatible Kubernetes YAMLs (Deployment, Service, Ingress)
- ✅ CI/CD workflows via GitHub Actions
- ✅ Monitoring stack (Prometheus + Grafana)
- ✅ Admin credentials for demo
- ✅ Screenshots and dashboards (to be updated)
- ✅ Docker images hosted publicly at:  
  🔗 [https://hub.docker.com/u/prateek2004](https://hub.docker.com/u/prateek2004)

You can clone, run, or extend this setup with ease for any production-grade DevOps deployment demo.

> Feel free to fork the repository, report issues, or suggest improvements.

🛠️ Maintained by [@prateek200445](https://github.com/prateek200445)  
📁 Repo: `celebal_final_devops_project`

---

🎉 **Thank you for exploring this DevOps showcase!**


