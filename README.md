# Application

This is an example of how to use Terraform to generate a project infrastructure, with Kubernetes and Jenkins for CI/CD. Terraform configures and generate all needed providers, communicating directly with the cloud provider, in this case Digital Ocean.

# How to run

## Prerequisites

In this case, we are using Windows:

- WSL2
- Docker Desktop
- Chocolatey
- Terraform

Also, you need an account in the Digital Ocean. After, you need to generate a SSH key and link it on Digital Ocean settings.

## Install k3d and kubernetes-cli

On terminal, as admin, input the followings commands:

```bash
choco install k3d
choco install kubernetes-cli
```

## Terraform usage

On terminal, as admin, input the followings commands:

```bash
git clone https://github.com/Henrickqt/terraform-digital-ocean.git
cd .\terraform-digital-ocean\
terraform init
terraform apply
```

After, you need to copy the output `kube_config.yaml` para `C:\Users\{your_user}\.kube\config`
