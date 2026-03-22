# 🚀 Kubernetes CKAD Practice Lab

> **Hafiz Naveed Uddin** — Agentic AI Developer | SOC Analyst | Full-Stack Engineer  
> 📍 Karachi, Pakistan &nbsp;|&nbsp; 4+ Years Experience &nbsp;|&nbsp; 19 Professional Certifications  
> 🌐 [Portfolio](https://naveed-portfolio-sigma.vercel.app/) &nbsp;|&nbsp; 💼 [LinkedIn](https://www.linkedin.com/in/hafiz-naveed-uddin-96072524b/)

---

## 📌 About This Project

This repository is a **hands-on Kubernetes practice lab** covering all five official **CKAD (Certified Kubernetes Application Developer)** exam domains. Every manifest is original, fully documented with inline comments, and built from scratch as part of my self-directed certification preparation.

I am applying for the **Linux Foundation LiFT Scholarship** to fund the CKAD exam. This project is my proof of readiness — I am already learning and practicing Kubernetes seriously, not just planning to.

---

## 🏅 Linux Foundation Certifications Completed

| Course | Date | Credential ID |
|--------|------|---------------|
| Introduction to Cloud Infrastructure Technologies (LFS151) | Dec 18, 2025 | LF-dsschskbfe |
| Introduction to RISC-V (LFD110) | Feb 28, 2026 | LF-tca2qyi3kr |

---

## 📁 Project Structure

```
ckad-kubernetes-project/
├── namespaces/            # Environment isolation (dev, staging, production)
├── pods/                  # Pods with probes, resource limits, security context
├── deployments/           # Rolling updates, rollback, sidecar pattern
├── services/              # ClusterIP, NodePort, LoadBalancer
├── configmaps/            # Application configuration management
├── jobs/                  # One-time Jobs and scheduled CronJobs
├── ingress/               # Path-based routing with Ingress rules
├── networkpolicies/       # Pod-level network isolation
└── docs/                  # CKAD exam cheatsheet & imperative commands
```

---

## 🗂️ CKAD Exam Domains Covered

| Domain | Topics | Files |
|--------|--------|-------|
| **Application Design & Build** | Multi-container pods, sidecar pattern | `pods/`, `deployments/sidecar-deployment.yaml` |
| **Application Deployment** | Rolling updates, rollback, scaling | `deployments/webapp-deployment.yaml` |
| **Application Observability & Maintenance** | Liveness & readiness probes, resource limits | `pods/webapp-pod.yaml` |
| **Application Environment, Config & Security** | ConfigMaps, SecurityContext, non-root containers | `configmaps/`, `pods/secure-pod.yaml` |
| **Services & Networking** | ClusterIP, NodePort, Ingress, NetworkPolicy | `services/`, `ingress/`, `networkpolicies/` |

---

## 🚀 Quick Start

```bash
# Clone the repo
git clone https://github.com/NAVEED261/ckad-kubernetes-project.git
cd ckad-kubernetes-project

# Create namespaces first
kubectl apply -f namespaces/

# Deploy sample app
kubectl apply -f configmaps/webapp-configmap.yaml -n dev
kubectl apply -f deployments/webapp-deployment.yaml -n dev
kubectl apply -f services/webapp-service.yaml -n dev

# Check status
kubectl get all -n dev
```

---

## 📚 Key Concepts Demonstrated

- **Rolling Update & Rollback** — zero-downtime deployments
- **Liveness & Readiness Probes** — health-check driven traffic routing
- **Security Context** — non-root containers with read-only filesystems
- **Sidecar Pattern** — multi-container log streaming via shared volumes
- **ConfigMaps** — config decoupled from container images
- **Jobs & CronJobs** — run-to-completion and scheduled workloads
- **NetworkPolicies** — micro-segmentation between frontend and backend
- **Ingress** — single-entry path-based routing to multiple services

---

## 👨‍💻 About the Author

I am a self-taught developer from Karachi, Pakistan with 4+ years of experience and **19 professional certifications** across AI, Cybersecurity, Cloud, and Data Science.

**Current Roles:**
- 🤖 Agentic AI Engineer @ PIAIC (Jan 2026–Present)
- 🛡️ SOC Analyst & Cybersecurity Professional (Jan 2024–Present)
- ⚡ Full-Stack Developer — Freelance & Open Source (Jun 2022–Present)

**Selected Certifications:**
- ✅ Certified Cloud Applied Generative AI Engineer — Governor Initiative & PIAIC (2025)
- ✅ Model Context Protocol Level 2 Developer — PIAIC (2026)
- ✅ IBM Cybersecurity Analyst — IBM / Coursera (2024)
- ✅ Certified in Cybersecurity — ISC2 (2024)
- ✅ SOC Analyst — EC-Council (2024)
- ✅ Introduction to Cloud Infrastructure Technologies LFS151 — Linux Foundation (2025)
- ✅ Introduction to RISC-V LFD110 — Linux Foundation (2026)

**Full profile & all 19 certifications:** [naveed-portfolio-sigma.vercel.app](https://naveed-portfolio-sigma.vercel.app/)

---

## 🌍 Why This Project Exists

The CKAD exam ($445) is not financially feasible for me without scholarship support. I built this project to prove that financial limitation has not stopped my learning. Every file here was written by hand, tested conceptually, and documented — as a demonstration of genuine commitment to the Kubernetes ecosystem and the Linux Foundation's open-source mission.

---

## 📜 License

MIT License — free to use, fork, and learn from.
