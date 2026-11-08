# criando-blog-azure-container-apps
Projeto prático de implantação de uma aplicação conteinerizada no Azure utilizando Azure Container Apps (ACA), Azure Container Registry (ACR) e Dockerfile para alta disponibilidade e escalabilidade.

# 🚀 Criando um Blog com Azure Container Apps

Projeto desenvolvido como parte do desafio prático da plataforma **DIO (Digital Innovation One)**, focado no provisionamento e deploy de aplicações conteinerizadas na nuvem Microsoft Azure.

---

## 📌 Visão Geral do Projeto
O objetivo deste projeto é demonstrar o ciclo completo de implantação de um blog conteinerizado no **Azure Container Apps**, desde a criação da imagem com Docker até o controle de revisões e segredos na nuvem.

### 🛠️ Tecnologias Utilizadas
* **Azure Container Apps (ACA):** Hospedagem e escalabilidade serverless baseada em Kubernetes.
* **Azure Container Registry (ACR):** Armazenamento privado e gerenciamento de imagens Docker.
* **Docker:** Conteinerização da aplicação.
* **Azure CLI:** Automação e execução dos comandos de infraestrutura.

---

## ⚙️ Passo a Passo do Desenvolvimento

### 1. Criação do Dockerfile
Construção do arquivo de imagem base para o ambiente do blog:
```dockerfile
FROM nginx:alpine
COPY ./src /usr/share/nginx/html
EXPOSE 80
