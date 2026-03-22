# End-to-End CI/CD DevOps Pipeline with Docker, Jenkins, Terraform, AWS & Kubernetes

## Overview

This project demonstrates a complete end-to-end DevOps pipeline that automates the process of building, containerizing, and deploying an application to cloud infrastructure. It integrates CI/CD practices with containerization, Infrastructure as Code (IaC), and Kubernetes-based orchestration.

The pipeline starts from source code in GitHub and progresses through Jenkins for continuous integration, Docker for containerization, Docker Hub for image storage, Terraform for infrastructure provisioning, and AWS EC2 for deployment. Kubernetes is used to simulate production-grade orchestration.

---

## Architecture

GitHub → Jenkins CI/CD → Docker → Docker Hub → Terraform → AWS EC2 → Kubernetes (Minikube)

---

## Features

* Automated CI/CD pipeline using Jenkins
* Containerization of application using Docker
* Versioned image storage in Docker Hub
* Infrastructure provisioning using Terraform (IaC)
* Deployment on AWS EC2 instances
* Kubernetes-based deployment using Minikube
* Automated application updates through pipeline execution
* Cloud-native architecture following DevOps best practices

---

## Tech Stack

* Cloud: AWS EC2
* Infrastructure as Code: Terraform
* CI/CD: Jenkins
* Containerization: Docker
* Container Registry: Docker Hub
* Orchestration: Kubernetes (Minikube)
* CLI Tools: kubectl
* Version Control: Git, GitHub
* OS: Linux (Ubuntu)

---

## Project Workflow

1. Developer pushes code to GitHub repository
2. Jenkins pipeline is triggered automatically
3. Docker image is built from application source
4. Image is pushed to Docker Hub
5. Terraform provisions infrastructure on AWS EC2
6. Jenkins deploys the latest image to EC2
7. Kubernetes manages container deployment and exposure

---

## Jenkins Pipeline Stages

* Source Code Checkout
* Docker Image Build
* Docker Image Push
* Deployment to EC2
* Kubernetes Deployment

---

## Infrastructure Details

* AWS EC2 instance provisioned using Terraform
* Security groups configured for HTTP and SSH access
* Docker runtime installed on EC2
* Kubernetes cluster created locally using Minikube

---

## Kubernetes Deployment

* Deployment object used for managing application pods
* Service object used for exposing application
* NodePort used for external access
* kubectl used for deployment automation

---

## How to Run

### Prerequisites

* Docker installed
* Jenkins installed
* AWS account configured
* Terraform installed
* kubectl and Minikube installed

### Steps

1. Clone the repository
2. Configure Jenkins pipeline with GitHub repository
3. Build and push Docker image
4. Apply Terraform configuration
5. Deploy application to EC2
6. Start Minikube and apply Kubernetes manifests

---

## Key Learnings

* Implementing CI/CD pipelines using Jenkins
* Working with Docker for application containerization
* Managing cloud infrastructure using Terraform
* Deploying applications on AWS EC2
* Understanding Kubernetes architecture and deployments
* Integrating multiple DevOps tools into a unified pipeline

---

## Future Improvements

* Migration to AWS EKS for managed Kubernetes
* Integration of monitoring tools like Prometheus and Grafana
* Implementation of GitOps using ArgoCD
* Adding Helm charts for Kubernetes deployments
* Auto-scaling and load balancing

---

## Author

Vaishnavi J P
DevOps
