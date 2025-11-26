#  Azure DevOps: Automated CI/CD Pipeline

This project demonstrates a complete **DevOps lifecycle** implementation using modern Infrastructure as Code (IaC) and automation tools. It deploys a containerized web application to an Azure Virtual Machine automatically upon code changes.

##  Architecture

```mermaid
graph LR
    User[Developer] -->|Push Code| GH[GitHub Repo]
    GH -->|Trigger| Action[GitHub Actions]
    subgraph Azure Cloud [Azure Spain Central]
        Action -->|SSH Deploy| VM[Ubuntu VM]
        VM -->|Pull| Docker[Docker Container]
        Terraform -->|Provision| VM
    end
Technologies Used
Category	Tool	Usage
Cloud Provider		Virtual Machines (B1s), Networking, NSG
IaC		Infrastructure Provisioning
Containerization		Application Containerization & Compose
CI/CD		Automated Deployment Pipeline
Scripting		Server Configuration Scripts

E-Tablolar'a aktar

Key Features
Infrastructure as Code: All Azure resources (Resource Groups, VM) are provisioned using Terraform.

Dockerized Application: The web server (Nginx) and services are containerized using Docker & Docker Compose.

Zero-Touch Deployment: A GitHub Actions pipeline automatically detects changes in the main branch, connects to the Azure server via SSH, and updates the containers with zero downtime strategies.

Security: SSH Keys are managed via GitHub Secrets; no hardcoded credentials.

How to Run
Clone the repo:

Bash

git clone [https://github.com/Phaerk/devops-bootcamp-spain.git](https://github.com/Phaerk/devops-bootcamp-spain.git)
Infrastructure Setup (Terraform): (Make sure you have Azure CLI and Terraform installed)

Bash

cd terraform-lab
terraform init && terraform apply
