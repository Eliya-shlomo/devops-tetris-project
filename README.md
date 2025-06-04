# 🚀 DevOps Project - AWS EKS, Terraform, Jenkins, ArgoCD
![](slides/slide0.png)

## 🌟 Overview
In this step-by-step guide, we take you through an exciting DevOps project where we deploy a fully functional Tetris game application on an AWS EKS (Elastic Kubernetes Service) cluster.
- **Use Terraform for creating and managing AWS infrastructure as code**
- **Set up Jenkins for a powerful CI/CD pipeline**
- **Implement ArgoCD for seamless GitOps deployment to Kubernetes**
- **Package Kubernetes resources with Helm**
- **Automated testing and builds via GitHub Actions**


## ✅ Slides

Slide 1            | Slide 2         | Slide 3       
:------------------------:|:-----------------------:|:----------------------:
![](slides/slide1.png)  | ![](slides/slide2.png) | ![](slides/slide3.png)

## 💻 Commands

```
aws eks update-kubeconfig --region us-east-1 --name Tetris-EKS-Cluster
```

```
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/v2.4.7/manifests/install.yaml
```

```
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}`
```

## 🔗 Links

### Terraform Installation

```
https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli
```
### AWSCLI Installation

```
https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html` 
```

### ArgoCD Initial Password

```
https://stackoverflow.com/questions/68297354/what-is-the-default-password-of-argocd
```

## 🛠️ Industry Tools

- Helm chart available under `helm/tetris` for simplified Kubernetes deployments.
- GitHub Actions workflow (`.github/workflows/ci.yml`) runs tests, builds Docker images and checks Terraform formatting on every push.

