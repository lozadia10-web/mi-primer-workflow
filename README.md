# CI/CD Pipeline: Despliegue Automatizado con Terraform & GitHub Actions 🚀

Este repositorio contiene un proyecto práctico de **Infraestructura como Código (IaC)** y **Despliegue Continuo (CD)**. El objetivo principal es automatizar el aprovisionamiento de un bucket de **AWS S3** configurado para hosting de sitios web estáticos y el despliegue automático del código frontend.

---

## 🛠️ Tecnologías y Servicios

* **Cloud Provider:** AWS (Amazon Web Services).
* **Infrastructure as Code (IaC):** [Terraform](https://www.terraform.io/) para la creación de recursos (S3 Buckets, Public Access Policies, Static Website Hosting).
* **CI/CD:** [GitHub Actions](https://github.com/features/actions) para la automatización del despliegue mediante el archivo `deploy.yml`.
* **Frontend:** HTML5 & CSS3.

---

## 🏗️ Arquitectura del Proyecto

El flujo de trabajo (Workflow) se activa automáticamente con cada `push` a la rama principal:

1.  **Checkout:** GitHub Actions descarga el código fuente.
2.  **Terraform Setup:** Se inicializa y aplica la configuración de infraestructura definida en `/infra/main.tf`.
3.  **Sync:** Se sincronizan los archivos de la carpeta `/app/` directamente con el bucket de S3 creado.

---

## 📁 Organización de Archivos

* `/.github/workflows/deploy.yml`: Definición del pipeline (pasos, secretos y comandos de AWS).
* `/app`: Código fuente del sitio web (HTML/CSS).
* `/infra`: Archivos de configuración de Terraform para definir la infraestructura en AWS.

---

## ⚙️ Requisitos Previos

Para replicar este proyecto, es necesario configurar los siguientes **Secrets** en el repositorio de GitHub:
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_REGION`

---
*Este proyecto es un entregable técnico para el curso de Cloud Computing, enfocado en la adopción de prácticas DevOps y automatización en la nube.*
