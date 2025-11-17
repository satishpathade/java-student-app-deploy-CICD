# Java Application CI/CD Pipeline using Jenkins, Maven

This repository contains a complete CI/CD pipeline that automates the process of building and deploying an application using Jenkins, Maven, and an EC2 server running Tomcat. The goal is to remove manual steps and create a smooth, repeatable deployment workflow.

---

## 🚀 What This Pipeline Does

1. GitHub Webhook detects a push and triggers Jenkins automatically  
2. Jenkins pulls the latest code  
3. Maven builds the application and creates a WAR file    
4. Securely uploads the WAR file to an EC2 server using SCP  
5. Deploys the build to Tomcat  
6. Restarts the service  
6. The updated Java application goes live without manual steps 

This gives a clean, automated CI/CD process with zero manual deployment steps.

---

## Architecture Overview


### **1. Repository Update**
A developer pushes new code to the GitHub repository.

### **2. GitHub Webhook Trigger**
GitHub sends a webhook request to Jenkins.  
This automatically starts the pipeline without manual action.

### **3. Checkout Code**
Jenkins pulls the latest code from the `main` branch.

### **4. Build with Maven**
Jenkins uses Maven to:
- Clean previous builds  
- Install dependencies  
- Compile Java code  
- Run lifecycle goals  
- Generate a WAR file in the `target/` directory  

### **5. Upload WAR to EC2**
Jenkins copies the WAR file to the EC2 instance using SCP and SSH.

### **6. Deploy on Tomcat**
On EC2:
- Tomcat stops  
- Old WAR is removed  
- New WAR is placed in the `webapps` folder  
- Tomcat starts again  

### **7. Application Live**
The updated Java application becomes available instantly.

---

## 🛠 Tech Stack

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

## 📄 Jenkinsfile (Full Pipeline)
**[jenkinsfile](jenkinsfile)**
This file contains the complete pipeline used for building and deploying the Java application.

---

## 👤 Author

**Satish Pathade**  
AWS Cloud & DevOps Engineer 

- GitHub: https://github.com/satishpathade  
- LinkedIn: https://www.linkedin.com/in/satish-pathade  
- Email: pathadesatish0@gmail.com
