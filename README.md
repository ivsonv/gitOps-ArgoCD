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