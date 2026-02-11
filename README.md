#  AWS ECS Fargate CI/CD Pipeline (CDK v2)

This project demonstrates an **end-to-end automated CI/CD pipeline** that deploys a **containerized Flask application** to **AWS ECS Fargate** using **AWS CDK (Infrastructure as Code).**

The goal of this project is to eliminate manual deployments by enabling a fully automated build-and-deploy workflow triggered directly from GitHub.

---

##  Architecture Overview

GitHub  
   ↓  
AWS CodePipeline  
   ↓  
AWS CodeBuild → Builds Docker image  
   ↓  
Amazon ECR → Stores the container image  
   ↓  
AWS ECS Fargate → Runs the application  
   ↓  
Application Load Balancer (ALB) → Exposes the app to the internet  



---

##  Tech Stack

- **Application:** Flask + Docker  
- **Container Registry:** Amazon ECR  
- **Compute:** AWS ECS Fargate (serverless containers)  
- **CI/CD:** AWS CodePipeline + CodeBuild  
- **Networking:** Application Load Balancer (ALB)  
- **Infrastructure as Code:** AWS CDK v2 (TypeScript)

---

##  What this project solves

This setup:

- Automates builds on every GitHub push  
- Packages the app as a Docker image  
- Stores images securely in ECR  
- Deploys updates automatically to ECS Fargate  
- Provides a public endpoint via ALB  
- Removes the need for manual deployments  

---

##  How deployment works (high level)

1. Developer pushes code to **GitHub**
2. **CodePipeline** detects the change  
3. **CodeBuild** builds the Docker image  
4. Image is pushed to **Amazon ECR**  
5. ECS Fargate updates the running service with a new task definition  
6. Application becomes live via the **Load Balancer**

---

##  Outcome

You get a production-style, automated cloud deployment workflow that mirrors real-world DevOps practices in many modern companies.

---






