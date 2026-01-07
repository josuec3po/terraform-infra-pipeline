# Terraform CI/CD Pipeline with GitHub Actions (AWS)

## Descrição

Este repositório contém um **projeto prático de estudo em DevOps e Infrastructure as Code**, 
desenvolvido **seguindo passo a passo um tutorial do canal Build & Run**, com foco na criação 
de uma pipeline completa de Terraform utilizando GitHub Actions e AWS.

O projeto foi realizado com o objetivo de **aprender na prática** os principais conceitos de:
- automação de infraestrutura
- CI/CD
- Terraform
- integração segura entre GitHub e AWS

---

## Arquitetura do Projeto

- Pipeline CI/CD com GitHub Actions
- Terraform para provisionamento de infraestrutura
- AWS como provedor de nuvem
- Backend remoto com S3 para statefile
- Lock de state para evitar concorrência
- Múltiplos ambientes:
  - `dev`
  - `prod`
- Deploy e destroy via pipeline

---

## Estrutura do Repositório

```terraform-infra-pipeline
.github/workflows/
  ├── terraform.yml
  └── deploy.yml

infra/
  ├── backend.tf
  ├── main.tf
  ├── provider.tf
  ├── variable.tf
  ├── destroy_config.json
  └── envs/
      ├── dev/
      │   └── terraform.tfvars
      └── prod/
          └── terraform.tfvars
