# GITOPS WITH ARGOCD

Argo CD is a declarative continuous delivery tool for Kubernetes. It can be used as a standalone tool or as part of your CI/CD workflow to deliver the resources your clusters need.

To manage infrastructure and application configurations in line with GitOps principles, your git repository must be your single source of truth. The desired state of your system must be versioned, expressed declaratively, and automatically retrieved.

## Requisites
* Golang - [go dev](https://go.dev/)
* kustomize.io [kustomize.io](https://kustomize.io)
* Kubernetes - K8s - [kubernetes.io](https://kubernetes.io/pt-br)
* Docker - [docker.io](https://hub.docker.com/)

## Commands
* go mod init apiCD

## Install Local With Docker
This guide assumes you have a grounding in the tools that Argo CD is based on. Please read understanding the basics to learn about these tools.
* ArgoCD - [Doc v2.12](https://argo-cd.readthedocs.io/en/stable/getting_started/)

### Requirements
* Installed kubectl command-line tool.
* Have a kubeconfig file (default location is `~/.kube/config)`.
_________________

1. Install Argo CD
  * kubectl create namespace argocd
  * kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
  * <img width="1391" alt="image" src="https://github.com/user-attachments/assets/fbb10f69-74ee-4253-8c4e-f26a77d53d42">

2. Install Argo CLI
  * brew install argocd (MAC)

3. Port Forwarding
  * kubectl port-forward svc/argocd-server -n argocd 8080:443
  * <img width="740" alt="image" src="https://github.com/user-attachments/assets/3fb1ada3-8807-403c-b1ac-e53b8e3a41e2">

4. Login Using The CLI
  * argocd admin initial-password -n argocd
  * <img width="782" alt="image" src="https://github.com/user-attachments/assets/7d27c9ab-08ab-4b72-bc10-af9f02a64e5e">

### Testing
* http://localhost:8080 *with -> _Port Forwarding_*
* login: admin
* password: -> `4. Login Using The CLI`

![image](https://github.com/user-attachments/assets/30068916-ac41-4e2c-a213-bdc6e2a99e54)

*_connected_*
![image](https://github.com/user-attachments/assets/b6cce11c-89b9-48a7-9af4-a8dd05d6e003)



