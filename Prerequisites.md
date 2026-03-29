# ⛏️ Prerequisites for Deploying 2048 Game on AWS EKS

This guide covers all the required tools and configurations needed to deploy the 2048 application on an Amazon EKS (Elastic Kubernetes Service) cluster using Kubernetes.

---

## ✅ Required Tools

### 1️⃣ AWS CLI

**Why it is required:**  
AWS CLI is used to interact with AWS services from the terminal. It helps in configuring credentials and managing EKS clusters.

### 🔧 Installation
Download from official site (based on your OS):
```bash
https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
````

### 🔍 Verify Installation
```bash
aws --version
````

### 📌 Example Output:
```bash
aws-cli/2.x.x Python/3.x.x
````

### 🔐 Configure AWS CLI
```bash
aws configure
````

### Provide 
##### 1. AWS Access Key ID
##### 2. AWS Secret Access Key
##### 3. Default region (e.g., us-west-2)
##### 4. Default output format (e.g., json)

## 

### 2️⃣ kubectl

**Why it's needed:**  
kubectl is the command-line tool used to interact with Kubernetes clusters. It helps in deploying applications, managing resources, and checking cluster status.

#### 🔧 Installation:

**Download from official website based on your OS**
```bash
https://kubernetes.io/docs/tasks/tools/
````

#### 🔍 Verify Installation
```bash
kubectl version --client
````

#### 📌 Example Output:
````bash
Client Version: v1.xx.x
````


##

### 3️⃣ eksctl

**Why it's needed:**  
eksctl is a CLI tool that simplifies the creation and management of Amazon EKS clusters.

#### 🔧 Installation:

**Install Chocolatey**
**Chocolatey is a package manager for Windows that makes installing tools easier.**

```bash
Set-ExecutionPolicy Bypass -Scope Process -Force; `
[System.Net.ServicePointManager]::SecurityProtocol = `
[System.Net.ServicePointManager]::SecurityProtocol -bor 3072; `
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
````

#### Check the version 
```bash
choco -v
````

##
### 🔧 Install eksctl
```bash
choco install eksctl -y
````
##
### 🔍 Verify Installation
```bash
eksctl version
```

### 📌 Example Output:
```bash
eksctl version: 0.xxx.x
```

##
## 🎯Finally
### Before starting the project, ensure:
#### AWS CLI is installed and configured ✅
#### kubectl is installed ✅
#### eksctl is installed ✅









