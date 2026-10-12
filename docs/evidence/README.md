# Pet Clinic AKS Deployment Evidence

This directory contains screenshots documenting the successful deployment
of the Pet Clinic website to Azure Kubernetes Service (AKS).

## Evidence Index

| File | Description |
|---|---|
| `01-pet-clinic-live-website.png` | Pet Clinic website accessible through the Azure public IP address. |
| `02-pet-clinic-kubernetes-status.png` | Kubernetes deployment, running pods, and LoadBalancer service. |
| `03-pet-clinic-azure-aks-cluster.png` | Azure Kubernetes Service cluster configuration and status. |
| `04-pet-clinic-acr-image.png` | Pet Clinic container image tag stored in Azure Container Registry. |

## Deployment Details

| Property | Value |
|---|---|
| Application | Pet Clinic |
| Azure resource group | `pet-clinic-aks-rg` |
| AKS cluster | `pet-clinic-aks` |
| Azure region | `centralus` |
| Container registry | `petclinicacr3595.azurecr.io` |
| Container image | `pet-clinic:1.0` |
| Kubernetes replicas | 2 |
| Service type | LoadBalancer |
| HTTP port | 80 |
| Public website | http://57.167.3.11 |

## Validation Results

- The website loaded successfully in a browser.
- An HTTP request returned `200 OK`.
- The live page returned the expected title: `Pet Clinic | Care for Every Paw`.
- Both Kubernetes application replicas were running and ready.
- Azure Container Registry contained the `pet-clinic:1.0` image tag.

## Technologies Demonstrated

- Docker and NGINX
- Azure Container Registry (ACR)
- Azure Kubernetes Service (AKS)
- Kubernetes Deployments, Pods, and Services
- Azure Load Balancer
- Kubernetes readiness and liveness probes

These screenshots document the state observed during the deployment exercise.
Cloud resources may change or be removed after the evidence is captured.
