# Three-Tier Web Application Deployment on AWS EKS

## Overview

This repository presents a self-built Three-Tier Web Application deployed on AWS EKS as part of a hands-on DevOps learning initiative. The project demonstrates end-to-end implementation of cloud infrastructure provisioning, containerization, CI/CD automation, monitoring, and GitOps practices.

The application architecture consists of:

* **Frontend:** ReactJS
* **Backend:** NodeJS
* **Database:** MongoDB

The entire system is containerized using Docker and orchestrated with Kubernetes on Amazon EKS. The project was developed independently to gain practical, real-world experience in modern cloud-native DevOps workflows.

---

## Architecture Summary

* AWS IAM configuration for secure access management
* EC2 instance setup for tooling and CI/CD server
* Infrastructure provisioning using Terraform
* Docker-based containerization
* Amazon ECR for private image repository management
* Amazon EKS for Kubernetes orchestration
* AWS Load Balancer Controller for external traffic routing
* Jenkins for CI/CD automation
* Prometheus and Grafana for monitoring and observability
* ArgoCD for GitOps-based continuous deployment

---

## Project Structure

**Application-Code**
Contains the frontend and backend source code of the application.

**Jenkins-Pipeline-Code**
Includes Jenkins pipeline scripts for automated build, image push, and deployment workflows.

**Jenkins-Server-TF**
Terraform scripts used to provision Jenkins server infrastructure on AWS.

**Kubernetes-Manifests-Files**
Kubernetes YAML manifests used for deploying and managing the application within the EKS cluster.

---

## Tools & Technologies

* AWS (IAM, EC2, EKS, ECR, Load Balancer)
* Terraform
* Docker
* Kubernetes
* Jenkins
* Helm
* Prometheus
* Grafana
* ArgoCD
* AWS CLI
* kubectl
* eksctl

---

## Implementation Steps

### 1. IAM Configuration

* Created an IAM user with appropriate administrative permissions.
* Generated access keys and configured AWS CLI.

### 2. EC2 Setup

* Launched an Ubuntu EC2 instance.
* Configured secure SSH access for remote management.

### 3. Tool Installation

Installed required tools on the EC2 instance:

* AWS CLI v2
* Docker
* kubectl
* eksctl
* Helm

### 4. EKS Cluster Setup

* Created the EKS cluster using eksctl.
* Configured kubeconfig for cluster access.
* Verified worker node readiness.

### 5. CI/CD Setup

* Provisioned Jenkins infrastructure using Terraform.
* Configured automated pipelines for:

  * Docker image build
  * Image push to Amazon ECR
  * Deployment to EKS

### 6. Kubernetes Deployment

* Created a dedicated namespace.
* Applied Kubernetes manifests.
* Configured Deployments and Services.
* Implemented Load Balancer for external application access.

### 7. Monitoring & GitOps

* Installed Prometheus and Grafana using Helm.
* Configured dashboards for monitoring cluster metrics.
* Implemented GitOps workflow using ArgoCD for continuous deployment.

---

## Cleanup

* Deleted the EKS cluster using eksctl.
* Terminated EC2 instances.
* Removed Load Balancers and associated security groups to prevent unnecessary charges.

---

## Learning Outcome

This project provided hands-on experience in:

* Infrastructure as Code (Terraform)
* CI/CD pipeline automation
* Kubernetes cluster management
* Cloud networking and security fundamentals
* Monitoring and observability practices
* GitOps-based deployment workflows

This repository represents a foundational DevOps implementation showcasing practical experience with modern cloud-native technologies.
