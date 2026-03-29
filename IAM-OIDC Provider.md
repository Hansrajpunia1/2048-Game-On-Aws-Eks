# IAM-OIDC Provider
---

### ✅ What Is the **IAM OIDC Provider**?

 The **IAM OIDC** (OpenID Connect) **Provider acts as a link between AWS IAM and Kubernetes service accounts**.

It enables **Kubernetes pods** in your EKS cluster to **assume IAM roles securely without embedding AWS credentials** in your pods.

---

### 🧠 Why We Need?

Kubernetes does not natively provide a secure way to access AWS services like S3, DynamoDB, or Lambda.

By using **IAM OIDC** along with **IAM Roles for Service Accounts (IRSA)**, pods can get **temporary credentials securely**, eliminating the need for hardcoded keys.

---

## Commands to Set Up IAM OIDC Provider
### Set your cluster name
````bash
export cluster_name=demo-cluster
````
````bash
oidc_id=$(aws eks describe-cluster --name $cluster_name --query "cluster.identity.oidc.issuer" --output text | cut -d '/' -f 5)
````

## Check if an IAM OIDC provider is already configured:
````bash
aws iam list-open-id-connect-providers | grep $OIDC_ID | cut -d "/" -f4
````
### If it’s not configured, associate it with your EKS cluster, run the below command:
````bash
eksctl utils associate-iam-oidc-provider --cluster $cluster_name --approve
````
