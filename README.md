# 🚀 CI/CD Pipeline for Spring Boot + Angular Project

This repository contains the complete **CI/CD pipeline setup** for deploying a full-stack application built with **Spring Boot (backend)** and **Angular (frontend)** using tools like **Jenkins**, **Docker**, and **Docker Compose**.

## 📦 What’s Included

- 🐳 `Dockerfile` – to containerize the Spring Boot backend
- ⚙️ `docker-compose.yml` – to orchestrate multi-container setup (Angular + Spring Boot)
- 🔐 `.env` – for environment variables
- 🛠 `jenkinsfile` – for automating the CI/CD pipeline via Jenkins
- ☕ `pom.xml` – Maven project for backend dependency management
- `mvnw`, `mvnw.cmd` – Maven wrapper scripts for portability

---

## 🔁 CI/CD Pipeline Steps (Jenkins)

The Jenkins pipeline defined in `jenkinsfile` executes the following:

1. **Clone** the repository
2. **Build** the backend using Maven
3. **Build and package** the frontend Angular app
4. **Build Docker images** for both apps
5. **Push to Docker Hub** (optional configuration)
6. **Deploy** containers via Docker Compose

---

## 🐳 Dockerized Stack

The `docker-compose.yml` manages:
- A **Spring Boot API container**
- An **Angular frontend container**
- (Optionally) a **MySQL or PostgreSQL DB container** (if added)

Make sure Docker and Docker Compose are installed and running.

```bash
docker-compose up --build
```

---

## 📁 Folder Structure

```
├── docker-compose.yml          # Multi-service orchestration
├── dockerfile                  # Backend containerization
├── jenkinsfile                 # Jenkins pipeline config
├── .env                        # Environment configuration
├── pom.xml                     # Maven backend config
├── src/                        # Application source code
```

---

## ✅ Prerequisites

- Docker & Docker Compose
- Jenkins (locally or on Jenkins server)
- Node.js & Angular CLI (for local frontend testing)
- Java 11+ & Maven

---

## 🧪 Usage

### Local Development

1. Clone the repository  
2. Edit `.env` and `docker-compose.yml` as needed  
3. Run the full stack:

```bash
docker-compose up --build
```

### Jenkins Deployment

Ensure Jenkins has:
- Docker installed
- Git credentials configured
- Docker daemon access
- Optional: Docker Hub or artifact registry credentials

---

## 🔐 Environment Variables

Use the `.env` file to configure:
- Application ports
- DB credentials (if used)
- JWT secrets
- Build modes

---

## 🧭 Roadmap

- Add Nginx as a reverse proxy
- Add TLS certificates (Let's Encrypt or custom)
- Integrate SonarQube for code quality checks
- Add Kubernetes deployment manifests

---

## 🤝 Contributing

Feel free to fork the repo and submit a pull request. All contributions and suggestions are welcome!


---

Built with 💻 DevOps tools to streamline Spring Boot + Angular deployments.
