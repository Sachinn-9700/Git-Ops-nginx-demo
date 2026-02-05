
# 🚀 Git-Ops Nginx Demo

## 📌 Project Introduction

This project demonstrates a **simple GitOps-style deployment** of an Nginx application on Kubernetes.
A static HTML page is containerized using Docker and deployed via Kubernetes manifests, with updates managed by changing image versions in Git.

The project focuses on **Git-driven deployment state**, not on application complexity or CI automation.

---

## 🛠️ Technologies Used

* **Docker** – Containerizing the Nginx application
* **Nginx** – Serving static web content
* **Kubernetes** – Deployment and Service management
* **Git (GitOps approach)** – Source of truth for deployment state
* **Argo CD** – Used to sync Kubernetes state from Git *(deployment tool, not defined in this repo)*

---

## ✨ Features

* Static web application served via Nginx
* Docker image-based versioning
* Kubernetes Deployment with controlled replicas
* NodePort Service for external access
* Git-managed deployment updates (GitOps pattern)

---

## 🔄 The Process (Step-by-Step Flow)

1. **Application Content**

   * A static `index.html` file defines the application UI and version information.

2. **Containerization**

   * Nginx base image is used.
   * The HTML file is copied into the Nginx default web directory.

3. **Image Versioning**

   * Docker image is built and tagged manually (example: `v24`).
   * Version changes are reflected in the HTML and image tag.

4. **Kubernetes Deployment**

   * Deployment references a specific image tag.
   * Single replica is used for simplicity.

5. **Service Exposure**

   * NodePort service exposes the application externally.

6. **GitOps Sync**

   * Kubernetes manifests are stored in Git.
   * Argo CD monitors the repository and syncs changes to the cluster when manifests are updated.

---

## 🧠 What I Learned

* How Git acts as the **single source of truth** in a GitOps workflow
* Why immutable image tags are important for predictable deployments
* How Argo CD continuously reconciles desired vs actual state
* Keeping Kubernetes manifests minimal and readable

---

## ♻️ Reusable / Design Concepts

* **GitOps-driven deployments**
* **Immutable Docker image versioning**
* Declarative Kubernetes configuration
* Separation of application content and deployment logic

These concepts scale directly into larger GitOps-managed environments.

---

## 📈 Overall Growth

This project improved my understanding of:

* Practical GitOps workflows
* Kubernetes deployment lifecycle
* Explaining GitOps concepts clearly in interviews
* Designing minimal but realistic DevOps demo projects

---

## ▶️ Running the Project (High-Level)

* Build and push the Docker image
* Update the image tag in Kubernetes manifests
* Commit changes to Git
* Argo CD syncs the updated state to the cluster
* Access the app via NodePort

---
