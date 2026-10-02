<h1 align="center">
☁️ Multi-Cloud Architecture – AWS, Azure & GCP
</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Multi--Cloud-AWS%20%7C%20Azure%20%7C%20GCP-232F3E?style=for-the-badge&logo=icloud&logoColor=white" alt="Multi Cloud">
  <img src="https://img.shields.io/badge/Cloud-Architecture-0078D4?style=for-the-badge&logo=cloudflare&logoColor=white" alt="Cloud Architecture">
  <img src="https://img.shields.io/badge/DevOps-Terraform%20%7C%20Docker%20%7C%20Kubernetes-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="DevOps">
</p>

<h1 align="center">☁️ Multi-Cloud Architecture</h1>

<h3 align="center">
  AWS • Microsoft Azure • Google Cloud Platform
</h3>

<p align="center">
  <b>🌐 Cloud Architecture • ☁️ Infrastructure • 🔐 IAM • 🚀 DevOps • 📊 Monitoring</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white">
  <img src="https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white">
  <img src="https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white">
  <img src="https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white">
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
</p>

---

<p align="center">
  <i>Hands-on implementation and comparison of AWS, Azure & GCP cloud platforms</i>
</p>

---

## 👨‍💻 Project Information

| Details | Information |
|---|---|
| **Name** | Venu Gopala Reddy Eppala |
| **Assignment** | Multi Cloud Architecture and Hands on Practice |
| **Cloud Platforms** | AWS • Azure • GCP |
| **Focus** | Cloud Architecture • CLI • Networking • IAM • DevOps |

---

## 🎯 Objective

To understand **Multi-Cloud architecture** and gain practical experience with **AWS, Microsoft Azure, and Google Cloud Platform (GCP)** by comparing equivalent cloud services, creating basic cloud resources, using cloud CLI tools, and designing a simple multi-cloud architecture.

---

## 🛠️ Requirements

- AWS Account
- Microsoft Azure Account
- Google Cloud Account
- AWS CLI
- Azure CLI
- Google Cloud CLI
- Linux / Ubuntu recommended
- Git & GitHub

---

# 🌐 What is Multi-Cloud?

Multi-Cloud is an architecture where an organization uses services from **two or more cloud providers**, such as AWS, Azure, and GCP.

### Why Use Multiple Cloud Providers?

Common reasons include:

- Avoiding dependence on a single cloud provider
- Using specific services available from different providers
- Business continuity and disaster recovery
- Geographic requirements
- Using specialized cloud services
- Supporting acquisitions or different business units

---

# 🔄 Multi-Cloud vs Hybrid Cloud

| Feature | Multi-Cloud | Hybrid Cloud |
|---|---|---|
| Cloud Providers | Usually two or more | Can use one or more |
| On-Premises Infrastructure | Not required | Required |
| Main Concept | Multiple cloud providers | Cloud + on-premises |
| Example | AWS + Azure + GCP | AWS + Company Data Center |
| Main Purpose | Provider flexibility | Integrating private/on-premises infrastructure with cloud |

---

# ✅ Advantages of Multi-Cloud

- Provider flexibility
- Workload-specific cloud selection
- Disaster recovery options
- Geographic flexibility
- Access to different managed services
- Reduced dependency on one provider
- Support for different business requirements

# ⚠️ Challenges of Multi-Cloud

- Different IAM models
- Different networking architectures
- Different billing systems
- Multiple CLIs and APIs
- Monitoring across different platforms
- Security policy consistency
- Data transfer costs

---

# ☁️ Cloud Service Comparison

| Requirement | AWS | Azure | GCP |
|---|---|---|---|
| Virtual Machine | EC2 | Azure Virtual Machines | Compute Engine |
| Object Storage | S3 | Azure Blob Storage | Cloud Storage |
| Managed Database | Amazon RDS | Azure Database Services | Cloud SQL |
| Kubernetes | Amazon EKS | Azure Kubernetes Service | Google Kubernetes Engine |
| IAM | AWS IAM | Microsoft Entra ID / Azure RBAC | Cloud IAM |
| Monitoring | Amazon CloudWatch | Azure Monitor | Cloud Monitoring |
| Container Registry | Amazon ECR | Azure Container Registry | Artifact Registry |



---

# 📋 Task 1: Cloud Service Comparison

## Virtual Machines

- **AWS EC2** – Provides scalable virtual servers.
- **Azure Virtual Machines** – Provides configurable virtual machines.
- **GCP Compute Engine** – Provides customizable virtual machine instances.

## Object Storage

- **Amazon S3** – Stores objects such as files, images, backups, logs, and static website content.
- **Azure Blob Storage** – Microsoft's object storage service.
- **Cloud Storage** – GCP object storage service.

## Managed Databases

- **Amazon RDS** – Managed relational database service.
- **Azure Database Services** – Managed database services provided by Azure.
- **Cloud SQL** – Managed relational database service from GCP.

## Kubernetes

- **Amazon EKS** – Managed Kubernetes service from AWS.
- **AKS** – Managed Kubernetes service from Azure.
- **GKE** – Managed Kubernetes service from Google Cloud.

## Container Registry

- **ECR** – AWS container image registry.
- **Azure Container Registry** – Azure container image registry.
- **Artifact Registry** – GCP service for storing and managing artifacts such as container images and packages.

### Outcome

> Understood the equivalent services across AWS, Azure, and GCP and their similar core purposes.

---

# 🟠 Task 2: AWS Hands-on

## AWS CLI Configuration

```bash
aws --version
aws configure
```

Verify identity:

```bash
aws sts get-caller-identity
```

---

## IAM User

### Console

1. Sign in to AWS Management Console.
2. Open **IAM**.
3. Select **Users**.
4. Click **Create user**.
5. Create the required user.
6. Configure permissions.

### CLI Verification

```bash
aws iam list-users
```

---

## EC2 Instance

### Console

1. Open **EC2 Dashboard**.
2. Click **Launch Instance**.
3. Name: `multi-cloud-vm`
4. Select Ubuntu AMI.
5. Select a small instance type.
6. Create/select a key pair.
7. Configure VPC and subnet.
8. Enable public IP if required.
9. Configure Security Group.
10. Allow SSH from **My IP**.
11. Launch the instance.

### CLI Verification

```bash
aws ec2 describe-instances
```

---

## S3 Bucket

### Console

1. Open **S3**.
2. Click **Create bucket**.
3. Enter a globally unique bucket name.
4. Select the AWS Region.
5. Keep **Block all public access** enabled.
6. Create the bucket.
7. Upload a test file.

### CLI Verification

```bash
aws s3 ls
```

---

## Security Group

Example configuration:

| Setting | Value |
|---|---|
| Name | `multi-cloud-sg` |
| Protocol | TCP |
| Port | 22 |
| Source | My IP |

### CLI Verification

```bash
aws ec2 describe-security-groups
```

---

## CloudWatch

Monitor EC2 metrics such as:

- CPU Utilization
- Network In
- Network Out
- Disk-related metrics where available

### CLI Verification

```bash
aws cloudwatch describe-alarms
```

### Outcome

> Successfully learned how to create and verify basic AWS resources including IAM, EC2, S3, Security Groups, and CloudWatch.

---

# 🔵 Task 3: Azure Hands-on

## Azure CLI

```bash
az --version
az login
az account show
az account list
```

---

## Resource Group

Create:

```text
Resource Group: multi-cloud-rg
```

### CLI Verification

```bash
az group list --output table
```

---

## Azure Virtual Machine

### Configuration

```text
Resource Group: multi-cloud-rg
VM Name: azure-lab-vm
Image: Ubuntu
Username: azureuser
Authentication: SSH Public Key
```

Configure:

- Virtual Network
- Subnet
- Public IP
- Network Security Group
- SSH access

### CLI Verification

```bash
az vm list --output table
```

---

## Storage Account

Create a globally unique storage account.

Example:

```text
venumulticloud2026
```

### CLI Verification

```bash
az storage account list --output table
```

---

## Network Security Group

Example:

```text
Name: azure-lab-nsg
Rule: SSH
Port: 22
Source: My IP
```

### CLI Verification

```bash
az network nsg list --output table
```

---

## Azure Monitor

Monitor:

- Percentage CPU
- Network In Total
- Network Out Total
- Disk metrics where available

### Outcome

> Learned the Azure resource hierarchy and created basic resources using Azure Portal and Azure CLI.

---

# 🟢 Task 4: GCP Hands-on

## GCP CLI

```bash
gcloud version
gcloud auth login
gcloud projects list
```

Set the active project:

```bash
gcloud config set project PROJECT_ID
```

---

## GCP Project

Create a project from:

```text
Google Cloud Console
        ↓
Project Selector
        ↓
New Project
```

Example project name:

```text
Multi Cloud Lab
```

Verify:

```bash
gcloud projects list
```

---

## Compute Engine VM

Example:

```text
Name: gcp-lab-vm
Region: asia-south1
Zone: asia-south1-a
OS: Ubuntu
```

### CLI Verification

```bash
gcloud compute instances list
```

---

## Cloud Storage

Create a globally unique bucket.

Example:

```text
venu-gcp-multicloud-2026
```

Keep public access prevention enabled.

### CLI Verification

```bash
gcloud storage buckets list
```

---

## Firewall Rule

Example:

```text
Name: allow-ssh-lab
Network: default
Direction: Ingress
Source: YOUR_PUBLIC_IP/32
Protocol: TCP
Port: 22
```

### CLI Verification

```bash
gcloud compute firewall-rules list
```

---

## Cloud Monitoring

Use **Metrics Explorer** to view:

- CPU utilization
- Network traffic
- Disk metrics

### CLI Verification

```bash
gcloud monitoring metrics-descriptors list
```

### Outcome

> Learned the relationship between Project, Region, Zone, and Resources, and practiced creating Compute Engine, Cloud Storage, firewall, and monitoring resources.

---

# 💻 Task 5: CLI Practice

## AWS

```bash
aws --version
aws configure
aws sts get-caller-identity
aws ec2 describe-instances
aws s3 ls
aws iam list-users
```

## Azure

```bash
az --version
az login
az account show
az group list --output table
az vm list --output table
az storage account list --output table
```

## GCP

```bash
gcloud version
gcloud auth login
gcloud projects list
gcloud compute instances list
gcloud storage buckets list
```

### Outcome

> Practiced the basic command-line interfaces of AWS, Azure, and GCP and learned how to authenticate and list cloud resources.

---

# 🏗️ Task 6: Multi-Cloud Architecture

```text
                         USERS
                           |
                           v
                  GLOBAL DNS / TRAFFIC
                           |
          +----------------+----------------+
          |                |                |
          v                v                v
        AWS              AZURE             GCP
          |                |                |
       ELB/LB           Load Balancer       LB
          |                |                |
      EC2 / ASG        VM / VMSS          GKE / VM
          |                |                |
         RDS          Azure Database      Cloud SQL
          |                |                |
         S3           Blob Storage       Cloud Storage
          |                |                |
          +----------------+----------------+
                           |
                           v
                 CENTRAL MONITORING
                           |
                           v
                 LOGGING / OPERATIONS
```

## Example Workload Distribution

### AWS

Primary application infrastructure.

### Azure

Microsoft-oriented enterprise workloads.

### GCP

Data, analytics, or backup workloads.

The assignment uses these as example workload distributions rather than universal provider recommendations.

---

# 🔧 Task 7: DevOps Perspective

## Terraform / OpenTofu

Infrastructure can be managed as code across:

```text
              GitHub
                 |
              Terraform
                 |
       +---------+---------+
       |         |         |
      AWS      Azure      GCP
```

Benefits:

- Infrastructure as Code
- Version control
- Repeatability
- Automation
- Standardized deployment

---

## Docker

```text
Application
     |
Docker Image
     |
Container Registry
     |
+----+----+
|    |    |
AWS Azure GCP
```

Containerization helps provide a consistent application runtime across environments.

---

## Kubernetes

Managed Kubernetes services:

| Cloud | Kubernetes |
|---|---|
| AWS | EKS |
| Azure | AKS |
| GCP | GKE |

Common Kubernetes concepts:

- Deployments
- Services
- ConfigMaps
- Secrets
- Ingress
- Namespaces
- Probes

---

## Jenkins

Centralized CI/CD:

```text
Developer
    |
  GitHub
    |
  Jenkins
    |
+---+---+---+
|   |   |   |
AWS Azure GCP
```

---

## GitHub Actions

GitHub Actions can deploy workloads to multiple cloud environments using separate workflows or deployment jobs.

```text
GitHub
   |
GitHub Actions
   |
+--+--+--+
|  |  |
AWS Azure GCP
```

---

## Prometheus & Grafana

Prometheus can collect metrics from different environments, while Grafana can provide centralized dashboards.

```text
AWS Metrics ----\
Azure Metrics --- > Prometheus ---> Grafana
GCP Metrics ----/
```

---

## Centralized Logging

Logs from different environments can be collected into a centralized logging platform.

```text
AWS Logs -------\
Azure Logs ------> Central Logging Platform
GCP Logs -------/
```

Centralized logging makes it easier to search and correlate application and infrastructure events.

---

## Secrets Management

| Cloud | Secret Management |
|---|---|
| AWS | AWS Secrets Manager |
| Azure | Azure Key Vault |
| GCP | Secret Manager |

Secrets should not be hard-coded into:

- Git repositories
- Dockerfiles
- Kubernetes manifests
- CI/CD configuration

---

# 🚀 Multi-Cloud CI/CD

```text
Developer
    |
  GitHub
    |
 CI/CD Pipeline
    |
 +-------------------+
 | Build             |
 | Test              |
 | Security Scan     |
 | Docker Build      |
 | Push Image        |
 +-------------------+
    |
 +--+--------+--------+
 |           |        |
AWS        Azure     GCP
```

Security tools such as:

- Trivy
- Snyk
- SonarQube

can be incorporated into the CI/CD pipeline.

---

# 📸 Screenshots

Recommended project structure:

```text
multicloud-architecture/
│
├── README.md
│
├── screenshots/
│   ├── aws/
│   │   ├── iam-user.png
│   │   ├── ec2.png
│   │   ├── s3.png
│   │   ├── security-group.png
│   │   └── cloudwatch.png
│   │
│   ├── azure/
│   │   ├── resource-group.png
│   │   ├── vm.png
│   │   ├── storage.png
│   │   ├── nsg.png
│   │   └── monitor.png
│   │
│   ├── gcp/
│   │   ├── project.png
│   │   ├── compute-engine.png
│   │   ├── storage.png
│   │   ├── firewall.png
│   │   └── monitoring.png
│   │
│   └── architecture/
│       └── multicloud-architecture.png
│
└── docs/
    └── assignment.md
```

---

# 📚 Key Learnings

Through this assignment, I practiced:

- Multi-Cloud architecture concepts
- AWS, Azure, and GCP service comparison
- IAM and access management
- Cloud networking
- Virtual machines
- Object storage
- Security Groups, NSGs, and firewall rules
- Cloud monitoring
- AWS CLI
- Azure CLI
- Google Cloud CLI
- Terraform/OpenTofu
- Docker
- Kubernetes
- Jenkins
- GitHub Actions
- Prometheus
- Grafana
- Centralized logging
- Cloud secrets management

---

# 📊 AWS vs Azure vs GCP

| Area | AWS | Azure | GCP |
|---|---|---|---|
| Compute | EC2 | Virtual Machines | Compute Engine |
| Storage | S3 | Blob Storage | Cloud Storage |
| Database | RDS | Azure Database Services | Cloud SQL |
| Kubernetes | EKS | AKS | GKE |
| IAM | AWS IAM | Entra ID / RBAC | Cloud IAM |
| Monitoring | CloudWatch | Azure Monitor | Cloud Monitoring |
| Registry | ECR | ACR | Artifact Registry |
| CLI | AWS CLI | Azure CLI | gcloud CLI |

---

# 📁 Deliverables

- [x] Multi-Cloud service comparison
- [x] AWS hands-on practice
- [x] Azure hands-on practice
- [x] GCP hands-on practice
- [x] CLI verification
- [x] Multi-Cloud architecture
- [x] DevOps perspective
- [ ] Screenshots
- [ ] Architecture diagram image
- [ ] GitHub repository

---

# 🎯 Overall Outcome

> Gained practical knowledge of **Multi-Cloud architecture across AWS, Azure, and GCP**, including cloud services, CLI tools, networking, IAM, monitoring, and DevOps tools such as **Terraform, Docker, Kubernetes, Jenkins, and GitHub Actions**.

---

# 👨‍💻 Author

**Venu Gopala Reddy Eppala**

### Technologies

```text
AWS • Microsoft Azure • GCP
Terraform • Docker • Kubernetes
Jenkins • GitHub Actions
Prometheus • Grafana
Linux • Git • CLI
```

---

## ⭐ Project Status

```text
AWS              ✅ Completed
Azure            ✅ Completed
GCP              ✅ Completed
CLI Practice     ✅ Completed
Architecture     ✅ Completed
DevOps           ✅ Completed
Documentation    ✅ Completed
```

---

<p align="center">

### ☁️ Multi-Cloud • DevOps • Cloud Engineering

**Created by Venu Gopala Reddy Eppala**

</p>
