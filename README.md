# 🍽️ Food Fiesta

## 🚀 CI/CD Deployment with Jenkins, Docker, Kubernetes, AWS EC2 & Nginx Reverse Proxy

Food Fiesta is a Spring Boot web application deployed using an end-to-end DevOps CI/CD workflow.

This project demonstrates how a Spring Boot application can be automatically built, containerized, pushed to a container registry, deployed to a self-managed Kubernetes cluster on AWS EC2, and accessed through an Nginx Reverse Proxy.

---

## 🏗️ Project Architecture

![Food Fiesta CI/CD Architecture](screenshot/food-fiesta-cicd-architecture.png)

## 🔄 Complete CI/CD Flow

```text
Developer
    ↓
GitHub
    ↓
Jenkins CI Pipeline
    ↓
Maven Build
    ↓
Docker Image Build
    ↓
Docker Hub
    ↓
Jenkins CD Pipeline
    ↓
Kubernetes Cluster on AWS EC2
    ↓
Spring Boot Application
    ↓
MySQL Database
```

### 🌐 Application Access

```text
User / Browser
      ↓
Nginx Reverse Proxy
      ↓
Kubernetes Service
      ↓
Spring Boot Application
      ↓
MySQL Database
```

---

## 🛠️ Technologies Used

- Java
- Spring Boot
- Maven
- Git & GitHub
- Jenkins
- Docker
- Docker Hub
- Kubernetes
- AWS EC2
- Nginx Reverse Proxy
- MySQL
- Linux

---

## 🔄 Jenkins CI Pipeline

The Continuous Integration pipeline automates the process of building and containerizing the Food Fiesta application.

### CI Pipeline Stages

1. Checkout source code from GitHub
2. Install required tools
3. Prepare the build environment
4. Build the Spring Boot application using Maven
5. Build the Docker image
6. Login to Docker Hub
7. Tag the Docker image
8. Push the Docker image to Docker Hub

![Jenkins CI Pipeline](./screenshot/jenkins-ci.png)

---

## 🚀 Jenkins CD Pipeline

The Continuous Deployment pipeline is responsible for deploying the application and database to the Kubernetes cluster running on AWS EC2.

### CD Pipeline Operations

- Checkout deployment configuration
- Prepare the deployment environment
- Deploy MySQL database
- Deploy Food Fiesta application
- Remove application when required
- Remove database when required
- Execute post-deployment actions

![Jenkins CD Pipeline](./screenshot/jenkins-cd.png)

---

## ☁️ AWS EC2 Infrastructure

The deployment infrastructure is hosted on AWS EC2.

The project uses separate EC2 instances for:

- Jenkins Server
- Kubernetes Control Plane
- Kubernetes Worker Node
- Nginx Reverse Proxy

```text
AWS Cloud
│
├── Jenkins Server (EC2)
├── Kubernetes Control Plane (EC2)
├── Kubernetes Worker Node (EC2)
└── Nginx Reverse Proxy (EC2)
```

![AWS EC2 Infrastructure](./screenshot/aws-ec2-instances.png)

---

## 🌐 Nginx Reverse Proxy

Nginx is used as a reverse proxy and acts as the entry point for users accessing the Food Fiesta application.

### Request Flow

```text
User / Browser
      ↓
Nginx Reverse Proxy
      ↓
Kubernetes Service
      ↓
Spring Boot Application
      ↓
MySQL Database
```

The Nginx Reverse Proxy forwards incoming client requests to the application running inside the Kubernetes cluster.

---

## 🍽️ Food Fiesta Application

After successful CI/CD execution, the Food Fiesta application is deployed to Kubernetes and made accessible through the Nginx Reverse Proxy.

![Food Fiesta Application](./screenshot/food-fiesta-application.png)

---

## 🔁 End-to-End DevOps Workflow

```text
Developer
    │
    ▼
GitHub
    │
    ▼
Jenkins CI Pipeline
    │
    ├── Maven Build
    ├── Docker Image Build
    ├── Docker Image Tag
    └── Push to Docker Hub
    │
    ▼
Docker Hub
    │
    ▼
Jenkins CD Pipeline
    │
    ▼
Kubernetes Cluster on AWS EC2
    │
    ├── Spring Boot Application
    │
    └── MySQL Database


User / Browser
    │
    ▼
Nginx Reverse Proxy
    │
    ▼
Kubernetes Service
    │
    ▼
Food Fiesta Application
    │
    ▼
MySQL Database
```

---

## 📸 Deployment Result

The Food Fiesta application is successfully:

- Built using Maven
- Containerized using Docker
- Pushed to Docker Hub
- Deployed using Jenkins CD
- Orchestrated using Kubernetes
- Hosted on AWS EC2
- Accessed through an Nginx Reverse Proxy

![Food Fiesta Application](./screenshot/food-fiesta-application.png)

---
