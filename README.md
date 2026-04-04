# 🚀 Full Stack DevOps Capstone Project



## 📌 Overview

This project demonstrates a complete **end-to-end DevOps lifecycle** including infrastructure provisioning, containerization, CI/CD automation, monitoring, logging, tracing, security, backup, and cost optimization.

---

## 🏗️ Architecture

```
Developer → GitHub → CI/CD Pipeline → Docker → Kubernetes Cluster
                                      ↓
                               Monitoring (Prometheus + Grafana)
                                      ↓
                         Logging (Loki + Promtail)
                                      ↓
                           Tracing (Jaeger)
```

---

## 📁 Project Structure

```
last/
 ├── README.md
 ├── infra/                 # Terraform configurations
 └── react-k8s-app/
      ├── k8s/              # Kubernetes manifests (Deployment, Service, HPA)
      │    └── app/
      ├── monitoring/       # Prometheus, Grafana, Loki, Promtail, Jaeger
      └── pipelines/        # CI/CD pipelines (GitHub Actions)
```

---

## ⚙️ Tech Stack

| Category         | Tools                        |
| ---------------- | ---------------------------- |
| Infrastructure   | Terraform                    |
| Containerization | Docker                       |
| Orchestration    | Kubernetes                   |
| CI/CD            | GitHub Actions               |
| Monitoring       | Prometheus, Grafana          |
| Logging          | Loki, Promtail               |
| Tracing          | Jaeger                       |
| Security         | IAM, Trivy, Network Policies |

---

## 🚀 Features

### 🏗️ Infrastructure Provisioning

* Provisioned infrastructure using Terraform
* Configured virtual network, subnets, and security groups
* Deployed Kubernetes cluster

---

### 🐳 Containerization & Orchestration

* Dockerized React web application
* Deployed containers to Kubernetes
* Configured Deployment, Service, and Ingress
* Implemented Horizontal Pod Autoscaler (HPA)

---

### ⚙️ CI/CD Pipeline

* Automated build and deployment using GitHub Actions
* Docker image build and push to registry
* Integrated vulnerability scanning using Trivy

---

### 📊 Monitoring & Observability

* Prometheus for metrics collection
* Grafana dashboards for visualization
* Alert rules configured

---

### 🔐 Security & Compliance

* IAM roles with least-privilege access
* Kubernetes Secrets for sensitive data
* Network Policies for traffic control
* Encryption at rest and in transit
* Container image scanning using Trivy

---

### 📜 Logging & Tracing

* Centralized logging using Loki and Promtail
* Log visualization in Grafana
* Distributed tracing using Jaeger

---

### 💾 Backup & Recovery

* Backup using Kubernetes YAML exports:

  ```
  kubectl get all -o yaml > backup.yaml
  kubectl get secrets -o yaml > secrets-backup.yaml
  ```
* Simulated failure and restored application
* Verified successful recovery

---

### 💰 Cost Optimization

* Analyzed usage using:

  ```
  kubectl top pods
  ```
* Implemented:

  * Resource right-sizing (CPU & memory)
  * Horizontal Pod Autoscaling (HPA)
  * Reduced replica count

---

## 🧪 How to Run

### 1️⃣ Clone Repository

```
git clone <your-repo-url>
cd last
```

---

### 2️⃣ Deploy Application

```
kubectl apply -f react-k8s-app/k8s/app/
```

---

### 3️⃣ Deploy Monitoring Stack

```
kubectl apply -f react-k8s-app/monitoring/
```

---

### 4️⃣ Verify Deployment

```
kubectl get pods
```

---

## 📊 Useful Commands

```
kubectl get pods
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl top pods
```

---

## 🔍 Observability Access

| Tool    | URL                    |
| ------- | ---------------------- |
| Grafana | http://localhost:3000  |
| Jaeger  | http://localhost:16686 |

---

## 🎯 Key Achievements

* End-to-end DevOps pipeline implementation
* Automated CI/CD workflow
* Scalable Kubernetes deployment
* Secure and compliant infrastructure
* Full observability (metrics, logs, tracing)
* Backup and recovery strategy
* Cost-efficient resource usage

---

## 🧠 Learnings

* Infrastructure as Code (Terraform)
* Kubernetes deployment and scaling
* CI/CD automation
* Monitoring and logging tools
* Security best practices

---

## 🚀 Future Improvements

* Implement HTTPS with TLS certificates
* Deploy on managed Kubernetes (EKS/GKE/AKS)
* Add Service Mesh (Istio/Linkerd)
* Integrate Slack/Email alerts
* Use Velero for automated backups

---

## 👨‍💻 Author

**Sanket Bhal**

---

⭐ If you like this project, give it a star!
