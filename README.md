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
