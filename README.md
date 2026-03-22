# 🚀 Kubernetes CKAD Practice Lab

A hands-on Kubernetes project covering all **CKAD (Certified Kubernetes Application Developer)** exam domains. Built as part of my preparation for the Linux Foundation CKAD certification.

## 👨‍💻 About This Project

This repository contains real-world Kubernetes manifests, deployment strategies, and configurations covering all topics tested in the CKAD exam. Each folder contains practical YAML files with comments explaining every field.

I completed the following Linux Foundation courses as prerequisites:
- ✅ **Introduction to Cloud Infrastructure Technologies (LFS151)**
- ✅ **Introduction to RISC-V (LFD110)**

---

## 📁 Project Structure

```
ckad-kubernetes-project/
├── namespaces/          # Namespace isolation examples
├── pods/                # Pod manifests with probes, resources, security
├── deployments/         # Rolling updates, rollbacks, scaling
├── services/            # ClusterIP, NodePort, LoadBalancer
├── configmaps/          # App configuration management
├── jobs/                # Jobs and CronJobs
├── ingress/             # Ingress rules and path-based routing
├── networkpolicies/     # Network isolation between pods
└── docs/                # Study notes and exam tips
```

---

## 🗂️ CKAD Exam Domains Covered

| Domain | Coverage | Folder |
|--------|----------|--------|
| Application Design & Build | ✅ | pods/, deployments/ |
| Application Deployment | ✅ | deployments/ |
| Application Observability & Maintenance | ✅ | pods/ (probes) |
| Application Environment, Config & Security | ✅ | configmaps/, pods/ |
| Services & Networking | ✅ | services/, ingress/, networkpolicies/ |

---

## 🛠️ Prerequisites

- Kubernetes cluster (minikube / kind / k3s)
- `kubectl` CLI installed
- Basic Linux command line knowledge

## 🚀 Quick Start

```bash
# Clone the repo
git clone https://github.com/hnaveed264/ckad-kubernetes-project.git
cd ckad-kubernetes-project

# Create namespaces first
kubectl apply -f namespaces/

# Deploy sample app
kubectl apply -f deployments/webapp-deployment.yaml
kubectl apply -f services/webapp-service.yaml

# Check status
kubectl get all -n dev
```

---

## 📚 Study Notes

See the [docs/](./docs/) folder for CKAD exam tips, imperative commands cheatsheet, and study notes.

---

## 🌍 Why This Project?

I am a self-taught developer from Karachi, Pakistan, working toward a career in cloud-native DevOps. This project is my practical proof of learning — built without any institutional support, purely out of passion for open-source technologies and the Kubernetes ecosystem.

---

## 📜 License

MIT License — free to use, fork, and learn from.
