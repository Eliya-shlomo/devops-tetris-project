# 🚀 DevOps Project - AWS EKS, Terraform, Jenkins, ArgoCD
![](slides/slide0.png)

## 🌟 Overview
In this step-by-step guide, we take you through an exciting DevOps project where we deploy a fully functional Tetris game application on an AWS EKS (Elastic Kubernetes Service) cluster.
- **Use Terraform for creating and managing AWS infrastructure as code**
- **Set up Jenkins for a powerful CI/CD pipeline**
- **Implement ArgoCD for seamless GitOps deployment to Kubernetes**


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


### Deploy with ArgoCD

Use the provided ArgoCD Application manifest to manage the game deployment.

```bash
kubectl apply -f argocd/tetris-app.yaml
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

