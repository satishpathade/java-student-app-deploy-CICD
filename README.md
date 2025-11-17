# Java Application CI/CD Pipeline using Jenkins, Maven

This repository contains a complete CI/CD pipeline that automates the process of building and deploying an application using Jenkins, Maven, and an EC2 server running Tomcat. The goal is to remove manual steps and create a smooth, repeatable deployment workflow.

---

## What This Pipeline Does

1. GitHub Webhook detects a push and triggers Jenkins automatically  
2. Jenkins pulls the latest code  
3. Maven builds the application and creates a WAR file    
4. Securely uploads the WAR file to an EC2 server using SCP  
5. Deploys the build to Tomcat  
6. Restarts the service  
6. The updated Java application goes live without manual steps 

This gives a clean, automated CI/CD process with zero manual deployment steps.

---

## Architecture 

**Push → GitHub Webhook → Jenkins → Maven Build → EC2 (Ubuntu) → Tomcat → Java App**
---

## Tech Stack

| Category | Technologies |
|---------|------------------------|
| **Language** | Java (WAR-based application) |
| **Build Tool** | Maven |
| **CI/CD** | Jenkins, **GitHub Webhook** |
| **Source Control** | Git & GitHub |
| **Deployment** | SSH, SCP |
| **Server** | AWS EC2 (Ubuntu) |
| **Application Server** | Apache Tomcat 10 |
| **Automation** | Jenkins Declarative Pipeline |

---

## Jenkinsfile (Full Pipeline)
**[jenkinsfile](jenkinsfile)**
This file contains the complete pipeline used for building and deploying the Java application.

---

## Author
**Satish Pathade**  
AWS Cloud & DevOps Engineer 

- GitHub: https://github.com/satishpathade  
- LinkedIn: https://www.linkedin.com/in/satish-pathade  
- Email: pathadesatish0@gmail.com
