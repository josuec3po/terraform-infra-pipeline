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
---
```

## O que foi aprendido com este projeto

* Criação de pipelines CI/CD com GitHub Actions
* Uso do Terraform para infraestrutura como código
* Separação de ambientes (dev/prod)
* Configuração de backend remoto no S3
* Uso de Assume Role (STS) para autenticação segura
* Execução de `plan`, `apply` e `destroy` via pipeline
* Boas práticas iniciais de DevOps

---

## Referência

Este projeto foi desenvolvido **seguindo o conteúdo educacional** do canal:

**Build & Run**
YouTube – Conteúdo focado em DevOps, Terraform e Cloud AWS.

Todo o crédito pela estrutura original e explicação do projeto pertence ao autor do conteúdo.
Este repositório tem **finalidade educacional e de aprendizado prático**.

---

## Observação

Este projeto **não foi criado do zero** e não representa uma solução de produção.
Ele foi utilizado como base de estudo para compreensão prática dos conceitos apresentados.

```
