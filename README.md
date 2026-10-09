# Portfolio

## [DevEx Environment Automation](https://github.com/ThomasMOwen/devex-env-automation)
This project aims to use docker compose to create a secure local DevEx environment. It uses the following:
- Git : Gitlab
- CI/CD : Jenkins
- Secrets Management : Hashicorp Vault
- Package Repository : Nexus

## [GitOps Platform](https://github.com/ThomasMOwen/gitops-platform)
A production-like internal developer platform bootstrapped from a single Git repository. Demonstrates GitOps principles using ArgoCD, with TLS, secrets management, ingress, and full cluster observability — all managed declaratively. Platform Components:
- ArgoCD: GitOps continuous delivery
- cert-manager:	Automated TLS certificate provisioning
- ingress-nginx:  Kubernetes ingress controller
- sealed-secrets: Encrypted secrets safe for Git
- kube-prometheus-stack: Metrics, dashboards, and alerting


## [Terraform Modules](https://github.com/ThomasMOwen/terraform-modules)
The aim of this project was to create a terraform config example that used local terraform modules, and a validation workflow to ensure security and validity of terraform config. It would be configured to run entirely within containers and would require no local installation other than Docker. Gitea was used to run the validation workflow. However, it can be switched to a GitHub action by creating the .github/workflows directory and moving the workflow file there. Platform components:
- Terraform: IaC Tool
- Trivy: Security scanning tool
- Tflint: Terraform linter
- Gitea: Repo and CI/CD tool, can be switched to GitHub and GitHub actions


## [Floci with Terraform](https://github.com/ThomasMOwen/floci-with-terraform)
The aim of this project was to create a terraform config example that used the Floci AWS emulator. The configuration will create a cluster in EKS to be used as a temporary environment, deploy some applications to the cluster and record metadata about the environment in S3. Variables will be used to define what and how many applications are to be deployed. The terraform workspace will use a remote backend in S3 simulated in Floci. The terraform commands required will be accessible using the env.sh script. It can be run entirely within containers and would not require local installations of Floci or Terraform. Platform components:
- Floci: AWS emulator
- Floci UI: UI Component for the Emulator
- Terraform: IaC Tool
