# 🚀 DevOps Project - AWS EKS, Terraform, Jenkins, ArgoCD
## 🌟 Overview
This repository demonstrates how to deploy a React-based Tetris game on AWS using modern DevOps practices.
- **Terraform** provisions the infrastructure as code.
- **Jenkins** builds Docker images and updates Kubernetes manifests.
- **ArgoCD** handles GitOps-based deployment to the cluster.

## 💻 Commands

```
aws eks update-kubeconfig --region us-east-1 --name Tetris-EKS-Cluster
```

```
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/v2.4.7/manifests/install.yaml
```

```
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
```

Apply the sample ArgoCD application:

```
kubectl apply -f argocd/application.yaml
```

## 🔗 Links

### Terraform Installation

```
https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli
```
### AWSCLI Installation

```
https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
```

### ArgoCD Initial Password

```
https://stackoverflow.com/questions/68297354/what-is-the-default-password-of-argocd
```

