# 🚀 AWS EKS + Kubernetes + ALB Project

This project demonstrates deployment of a cloud-native application on AWS EKS using Kubernetes and AWS Load Balancer Controller.

## 📌 Architecture
![Architecture](architecture/architecture.png)

## 🔧 Tech Stack
- AWS EKS
- Kubernetes
- Docker
- Helm
- AWS Load Balancer Controller
- eksctl & kubectl

## 🚀 Features
- EKS cluster setup using eksctl  
- IAM OIDC provider integration  
- ALB Controller installation using Helm  
- Kubernetes Deployment, Service & Ingress  
- Application exposed via Application Load Balancer  

## 📂 Project Structure
- `k8s/` → Kubernetes manifests  
- `images/` → Screenshots  
- `architecture/` → Architecture diagram  

## 🌐 Output
Application is accessible via ALB DNS.

## 📸 Screenshots
![App](images/app.png)
![ALB](images/alb.png)

## 📚 Steps
Follow detailed steps:
- [Prerequisites](Prerequisites.md)
- [IAM & OIDC](iam-oidcprovider.md)
- [Deployment](deployment.md)
- [Service](service.md)
- [ALB Controller](alb-controller.md)
