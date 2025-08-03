# 🏦 Azure Banking Cloud Platform

A comprehensive, end-to-end cloud platform for the **banking domain**, architected on Azure and Microsoft Fabric. This project provides a robust, scalable, and secure foundation for modern banking analytics, integrating Infrastructure-as-Code, CI/CD, and advanced data governance.

> 🚀 **Mission:** To deliver a production-grade, cloud-native banking data platform that accelerates insights from ingestion to analytics while ensuring security and compliance.

![Tech Stack Banner](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white) ![Tech Stack Banner](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white) ![Tech Stack Banner](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white) ![Tech Stack Banner](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![Tech Stack Banner](https://img.shields.io/badge/Microsoft_Fabric-5E2496?style=for-the-badge&logo=microsoft&logoColor=white) ![Tech Stack Banner](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black) ![Tech Stack Banner](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

---

## 📌 Key Features

*   **End-to-End Data Lifecycle:** Fully implemented data flow from raw data ingestion to interactive business intelligence dashboards.
*   **Hybrid Data Pipelines:** Leverages both real-time and batch processing using Azure Data Factory and Microsoft Fabric Notebooks.
*   **Infrastructure-as-Code (IaC):** All cloud resources are defined and managed using Terraform for repeatable and consistent environments.
*   **Automated CI/CD:** GitHub Actions workflows for automated testing and deployment of SQL schemas, infrastructure (Terraform), and Power BI reports.
*   **Containerized Development:** Utilizes SQL Server in Docker for local development, with seamless deployment to Azure Kubernetes Service (AKS) for production.
*   **Actionable BI Dashboards:** Pre-built Power BI reports for critical banking use-cases like fraud detection, ATM activity analysis, and loan approvals.
*   **Enterprise-Grade Security:** A security-first approach with data encryption, Azure Purview integration, data masking, and comprehensive threat detection.

---

## 📁 Repository Structure

```plaintext
azure-banking-cloud-platform/
│
├── 📂 bi/               # Power BI reports (.pbix), deployment configurations
├── 📂 data/             # Sample banking datasets (CSV, Parquet)
├── 📂 devops/           # GitHub Actions workflows (.yml), pipeline templates
├── 📂 docs/             # Detailed documentation (LIFECYCLE.md, ROADMAP.md)
├── 📂 etl/              # ETL/ELT logic: Fabric Notebooks, ADF pipeline JSON
├── 📂 infrastructure/   # Terraform modules, Dockerfiles, Kubernetes manifests
└── 📂 tests/            # Test scripts for SQL procedures, pipelines, and data quality```

---

## 🛠️ Technology Stack

| Layer                    | Primary Technologies                                      |
| ------------------------ | --------------------------------------------------------- |
| **Infrastructure & IaC** | Terraform, Docker, Azure Kubernetes Service (AKS)         |
| **Data Platform**        | Azure Data Factory, Microsoft Fabric (Notebooks, Dataflows) |
| **Databases**            | Azure SQL, Azure Database for PostgreSQL, SQL Server      |
| **Analytics & BI**       | Power BI (Desktop, Service, REST API), DAX, RLS           |
| **DevOps & Automation**  | GitHub Actions, Azure CLI, Power BI Deployment APIs       |
| **Governance & Security**| Azure Purview, Azure Key Vault, SQL Auditing              |

---

## 🧬 Data Lifecycle Architecture

The platform manages the complete data journey, ensuring integrity and value at every stage. For a detailed breakdown, see [docs/LIFECYCLE.md](docs/LIFECYCLE.md).

**📥 Ingestion** → **🧮 Transformation** → **🛢️ Storage** → **📊 Analysis & BI** → **🧑‍💼 Governance**

---

## 🚀 Getting Started

### Prerequisites
*   An active Azure Subscription
*   Azure CLI installed and configured
*   Terraform installed
*   Docker Desktop (for local development)
```
### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/azure-banking-cloud-platform.git
cd azure-banking-cloud-platform
```

### 2. Deploy the Infrastructure
The Terraform scripts will provision all the necessary Azure resources.
```bash
cd infrastructure/
terraform init
terraform apply
```

### 3. Run ETL & Analyze Data
Load Data: Use scripts in the data/ directory to load sample datasets.
Execute Pipelines: Trigger the Azure Data Factory pipelines from the Azure Portal or via CI/CD.
Explore Notebooks: Run data transformation and analysis notebooks in your Microsoft Fabric workspace.
View Dashboards: Open the .pbix files in the bi/ folder with Power BI Desktop or publish them to the Power BI Service.

### 4. 📊 Power BI Dashboard Previews
The platform includes several pre-configured dashboards for immediate insights.
💳 Fraud Detection by Region	🏧 ATM Cash Volume Heatmap	💼 Loan Approval Funnel
![alt text](https://via.placeholder.com/300x200.png?text=Fraud+D
Row-level security and certified dataset configurations are included.

### 5. 📦DevOps & CI/CD Automation
Our GitHub Actions pipelines automate key processes to ensure reliability and speed:
On Push to main: Triggers Terraform to apply infrastructure changes.
On Pull Request: Validates Terraform plans, runs SQL unit tests.
Manual Trigger: Deploys or updates Power BI reports using the REST API.
This approach enforces a PR-based approval flow for all production changes.

### 6. 📅 Project Roadmap
For a detailed list of future enhancements and development sprints, please see the official Project Roadmap. Key milestones include:
Initial Infra Setup (Terraform, Docker)
SQL Database Provisioning
Advanced ETL & Data Modeling
ML Model Integration for Fraud Scoring
Final Security & Performance Audits

