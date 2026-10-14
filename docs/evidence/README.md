# Pet Clinic AKS Deployment Evidence

This directory contains screenshots documenting the Pet Clinic website deployed to Azure Kubernetes Service (AKS), together with the verification results observed during the deployment exercise.

## Evidence Index

| File | Description |
|---|---|
| `01-pet-clinic-live-website.png` | Browser view of the deployed Pet Clinic website. |
| `02-pet-clinic-kubernetes-status.png` | Kubernetes Deployment, pod, and Service status. |
| `03-pet-clinic-azure-aks-cluster.png` | Azure Kubernetes Service cluster configuration. |
| `04-pet-clinic-acr-image.png` | Pet Clinic container image stored in Azure Container Registry. |
| `05-pet-clinic-ci-success.png` | Screenshot of the successful Pet Clinic CI workflow. |
| `06-pet-clinic-cd-success.png` | Screenshot of the successful Pet Clinic CD workflow. |

## Deployment Details

| Property | Value |
|---|---|
| Application | Pet Clinic |
| Azure resource group | `pet-clinic-aks-rg` |
| AKS cluster | `pet-clinic-aks` |
| Azure region | `centralus` |
| Container registry | `petclinicacr3595.azurecr.io` |
| Image name | `pet-clinic` |
| Application replicas | 2 |
| Proxy replicas | 1 |
| Public Service | `LoadBalancer` |
| Public ports | 80 and 443 |
| Public IP | `57.167.3.11` |
| Live website | [https://57.167.3.11/](https://57.167.3.11/) |

## Validation Results

The following results were observed during verification:

- Pet Clinic CI completed successfully.
- Pet Clinic CD completed successfully.
- The application Deployment reported 2/2 replicas ready.
- The NGINX proxy Deployment reported 1/1 replica ready.
- All three application and proxy pods were Running and Ready, with zero restarts reported at the time of inspection.
- The public LoadBalancer Service exposed ports 80 and 443 on `57.167.3.11`.
- An HTTPS request returned HTTP status `200`.
- TLS verification returned `0`, indicating successful certificate verification for that request.

These results describe the environment at the time of testing and are not a guarantee of future availability.

## Technologies Demonstrated

- Docker and NGINX
- Azure Container Registry (ACR)
- Azure Kubernetes Service (AKS)
- Kubernetes Deployments, Pods, and Services
- Azure Load Balancer
- GitHub Actions CI/CD
- Azure OIDC authentication
- HTTPS and Kubernetes TLS Secrets
- Automated HTML and Kubernetes manifest validation

## Certificate Note

The certificate used during this exercise was reported valid through 20 October 2026. Verify its current validity and renewal status before relying on the live endpoint.

## Resource and Cost Note

Azure resources may incur charges while they remain provisioned. When the exercise is complete, verify the resources to be removed before running any cleanup commands.
