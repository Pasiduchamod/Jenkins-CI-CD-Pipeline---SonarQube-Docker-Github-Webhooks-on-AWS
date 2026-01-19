"# 🚀 Jenkins CI/CD Pipeline with SonarQube, Docker & AWS

[![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)](https://www.jenkins.io/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?style=for-the-badge&logo=sonarqube&logoColor=white)](https://www.sonarqube.org/)
[![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/)

## 📋 Project Overview

A fully automated **CI/CD pipeline** built with industry-standard DevOps tools to demonstrate end-to-end software delivery automation. This project showcases the complete workflow from code commit to production deployment, including automated testing, code quality analysis, containerization, and cloud deployment.

## 🎯 Project Objectives

- ✅ Implement automated CI/CD workflow using Jenkins
- ✅ Integrate code quality and security analysis with SonarQube
- ✅ Containerize applications using Docker
- ✅ Deploy to AWS EC2 with zero downtime
- ✅ Configure GitHub webhooks for automatic build triggers
- ✅ Establish DevOps best practices and automation standards

## 🏗️ Architecture

The pipeline follows a **Build → Test → Analyze → Containerize → Deploy** workflow:

```
GitHub Repository (Code Push)
        ↓
    Webhook Trigger
        ↓
Jenkins Pipeline (Automated)
        ↓
    ┌───────────────────────────────────┐
    │  1. Build Stage                   │
    │  2. Code Quality (SonarQube)      │
    │  3. Docker Image Build & Push     │
    │  4. Deploy to AWS EC2             │
    └───────────────────────────────────┘
        ↓
Application Running on AWS
```

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **Jenkins** | CI/CD automation server |
| **GitHub** | Version control & webhook integration |
| **Docker** | Application containerization |
| **SonarQube** | Static code analysis & quality gates |
| **AWS EC2** | Cloud deployment platform |
| **Git** | Source code management |

## ✨ Key Features

- **Automated Pipeline**: Triggered automatically on every code push via GitHub webhooks
- **Code Quality Gates**: SonarQube integration for maintaining code standards
- **Containerization**: Docker images for consistent deployment across environments
- **Cloud Deployment**: Automated deployment to AWS EC2 instances
- **Pipeline Visualization**: Clear view of all stages (Build → Test → Deploy)
- **Scalable Architecture**: Easily extendable for additional stages or environments

## 📸 Screenshots

### 1️⃣ Jenkins Pipeline View
Complete pipeline with all stages visible: Build → Test → Docker → Deploy

![Jenkins Pipeline](screenshots/Jenkins%20pipeline%20view.png)

---

### 2️⃣ Successful Build
Green status indicating successful pipeline execution

![Successful Build](screenshots/Successful%20build%20log.png)

---

### 3️⃣ SonarQube Quality Gate
Code quality analysis dashboard showing passed quality gates

![SonarQube Dashboard](screenshots/SonarQube%20dashboard.png)

---

### 4️⃣ Docker Images
Docker images created and managed in Jenkins

![Docker Image 1](screenshots/Docker%20image%20in%20Jenkins(1).png)
![Docker Image 2](screenshots/Docker%20image%20in%20Jenkins(2).png)

---

### 5️⃣ AWS EC2 Instance
Application successfully deployed and running on AWS EC2

![EC2 Instance](screenshots/EC2%20instance.png)
![App Running](screenshots/App%20running%20on%20AWS%20EC2.png)

## 🚦 Pipeline Stages

### Stage 1: Build
- Pull latest code from GitHub repository
- Compile/build the application
- Resolve dependencies

### Stage 2: Code Quality Analysis
- Run SonarQube scanner
- Analyze code quality, bugs, vulnerabilities
- Check against quality gate rules

### Stage 3: Docker Build & Push
- Build Docker image with application
- Tag the image appropriately
- Push to Docker registry (Docker Hub/ECR)

### Stage 4: Deploy to AWS
- Pull Docker image on EC2 instance
- Stop old container (if running)
- Start new container with updated image
- Verify deployment success

## 📦 Project Structure

```
Jenkins-CICD-Pipeline/
├── index.html              # Sample application
├── Dockerfile              # Docker configuration
├── Jenkinsfile             # Pipeline definition
├── sonar-project.properties # SonarQube configuration
├── screenshots/            # Project screenshots
└── README.md              # Project documentation
```

## 🔧 Setup & Configuration

### Prerequisites
- AWS account with EC2 access
- Jenkins server installed and configured
- Docker installed on Jenkins server
- SonarQube server setup
- GitHub repository with webhook access

### Installation Steps

1. **Configure Jenkins**
   ```bash
   # Install required plugins
   - Docker Pipeline
   - SonarQube Scanner
   - GitHub Integration
   ```

2. **Setup SonarQube**
   ```bash
   # Create project in SonarQube
   # Generate authentication token
   # Configure in Jenkins credentials
   ```

3. **Configure GitHub Webhook**
   ```
   Repository → Settings → Webhooks
   Payload URL: http://<jenkins-url>/github-webhook/
   ```

4. **Setup AWS EC2**
   ```bash
   # Launch EC2 instance
   # Install Docker
   # Configure security groups (ports 80, 443, 8080)
   # Setup SSH keys for Jenkins access
   ```

## 🎓 Learning Outcomes

- ✅ Hands-on experience with CI/CD pipeline design and implementation
- ✅ Understanding of automated testing and code quality gates
- ✅ Docker containerization for deployment consistency
- ✅ AWS cloud deployment strategies
- ✅ Jenkins pipeline scripting and automation
- ✅ Integration of multiple DevOps tools in a cohesive workflow

## 🔐 Security Considerations

- Credentials stored securely in Jenkins Credentials Manager
- SonarQube quality gates prevent poor code from deployment
- Docker images scanned for vulnerabilities
- AWS security groups configured with minimal required access
- SSH keys used for secure EC2 access

## 💡 Key Takeaways

This project demonstrates:
- **Automation First**: Complete automation from code commit to deployment
- **Quality Assurance**: Built-in code quality checks preventing bad code deployment
- **Modern Practices**: Containerization and cloud-native deployment
- **DevOps Culture**: Breaking down silos between development and operations
- **Scalability**: Foundation for enterprise-grade CI/CD pipelines

---

## 📝 License

This project is open source and available for educational purposes.

---

**⭐ If you found this project helpful, please consider giving it a star!**" 
