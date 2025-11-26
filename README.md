Harika, en doğrusu bu. Kodlarda hiçbir bozulma olmaması için senin **Phaerk** kullanıcı adına ve **devops-bootcamp-spain** repona özel, kopyala-yapıştır yapabileceğin en temiz hali hazırladım.

Aşağıdaki kod bloğunu **sağ üst köşesindeki "Copy" butonuna basarak kopyala**, GitHub'daki `README.md` dosyasının içine gir, **her şeyi sil** ve bunu yapıştır.

````markdown
# 🚀 Azure DevOps: Automated CI/CD Pipeline

This project demonstrates a complete **DevOps lifecycle** implementation using modern Infrastructure as Code (IaC) and automation tools. It deploys a containerized web application to an Azure Virtual Machine automatically upon code changes.

## 🏗️ Architecture

```mermaid
graph LR
    User[Developer] -->|Push Code| GH[GitHub Repo]
    GH -->|Trigger| Action[GitHub Actions]
    subgraph Azure Cloud [Azure Spain Central]
        Action -->|SSH Deploy| VM[Ubuntu VM]
        VM -->|Pull| Docker[Docker Container]
        Terraform -->|Provision| VM
    end
````

## 🛠️ Technologies Used

| Category | Tool | Usage |
|----------|------|-------|
| **Cloud Provider** |  | Virtual Machines (B1s), Networking, NSG |
| **IaC** |  | Infrastructure Provisioning |
| **Containerization** |  | Application Containerization & Compose |
| **CI/CD** |  | Automated Deployment Pipeline |
| **Scripting** |  | Server Configuration Scripts |

## ⚙️ Key Features

  * **Infrastructure as Code:** All Azure resources (Resource Groups, VM) are provisioned using Terraform.
  * **Dockerized Application:** The web server (Nginx) and services are containerized using Docker & Docker Compose.
  * **Zero-Touch Deployment:** A GitHub Actions pipeline automatically detects changes in the `main` branch, connects to the Azure server via SSH, and updates the containers with zero downtime strategies.
  * **Security:** SSH Keys are managed via GitHub Secrets; no hardcoded credentials.

## 🚀 How to Run

1.  **Clone the repo:**

    ```bash
    git clone [https://github.com/Phaerk/devops-bootcamp-spain.git](https://github.com/Phaerk/devops-bootcamp-spain.git)
    ```

2.  **Infrastructure Setup (Terraform):**
    *(Make sure you have Azure CLI and Terraform installed)*

    ```bash
    cd terraform-lab
    terraform init && terraform apply
    ```

3.  **Deployment:**
    The CI/CD pipeline handles the rest automatically on push\!

<!-- end list -->

```

### 📝 Nasıl Yapacaksın?

1.  GitHub'da **devops-bootcamp-spain** repona git.
2.  `README.md` dosyasının sağındaki **Kalem (Edit)** ikonuna tıkla.
3.  İçeride ne varsa hepsini sil (boş olsun).
4.  Yukarıdaki kodu yapıştır.
5.  Sayfanın en altına in ve yeşil **Commit changes** butonuna bas.

Şimdi profilin harika görünecek! 🚀
```
