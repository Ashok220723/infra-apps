# 🚀 CI/CD Stack with Docker Compose

This project provides a set of production-ready `docker-compose.yml` files to deploy a complete, isolated **CI/CD stack** on your local machine.  

The setup includes:
- **Jenkins** for automation  
- **Nexus** for artifact management  
- **SonarQube** for code quality analysis  
- **Nginx reverse proxy** for unified access  

---

## 📦 Project Components

This stack is built using the following services, each running in its own container:

- **Jenkins**: Automation server for build, test, and deployment pipelines. Persistent volume stores all job data.  
- **Nexus Repository Manager**: Central artifact repository for managing project dependencies (Maven, npm, etc).  
- **SonarQube**: Code quality and security analysis. Backed by PostgreSQL database for persistence.  
- **Nginx Reverse Proxy**: Routes requests based on domain names. Provides single entry point for all services.  

---

## ✅ Prerequisites

Make sure you have:

- [Docker](https://docs.docker.com/get-docker/)  
- [Docker Compose](https://docs.docker.com/compose/install/)  
- A text editor (e.g., VS Code)  

---

## ⚙️ Setup and Running the Stack

### Step 1: Clone or Prepare Files

Create a new project directory and add the following files:

- `docker-compose-jenkins.yml`  
- `docker-compose-nexus.yml`  
- `docker-compose-sonarqube.yml`  
- `docker-compose-nginx.yml`  
- `nginx.conf`  

Full examples provided below.  

---

### Step 2: Create a Shared Docker Network

```bash
docker network create ci-cd-network
