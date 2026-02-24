# MEAN Stack Cloud Deployment (Docker + CI/CD)

## 📌 Project Overview

This project demonstrates containerization and cloud deployment of a full-stack MEAN (MongoDB, Express, Angular, Node.js) application using Docker, Docker Compose, GitHub Actions, AWS EC2, and Nginx.

The application is fully containerized and deployed on a cloud-based Ubuntu virtual machine with CI/CD automation.

---

## 🏗️ Architecture

GitHub → GitHub Actions → Docker Hub → AWS EC2 (Ubuntu) → Docker Compose → Nginx → Browser

---

## 🚀 Tech Stack

- MongoDB
- Express.js
- Angular
- Node.js
- Docker
- Docker Compose
- GitHub Actions (CI/CD)
- AWS EC2
- Nginx

---

## 📂 Project Structure

```
mean-devops-assignment/
│
├── frontend/
│   └── Dockerfile
│
├── backend/
│   └── Dockerfile
│
├── docker-compose.yml
│
└── .github/
    └── workflows/
        └── deploy.yml
```

---

## 🐳 Containerization

### Backend
- Node.js 18 base image
- Dependency installation
- Exposed on port 5000

### Frontend
- Multi-stage Docker build
- Angular production build
- Served via Nginx
- Exposed on port 80

---

## 🗄️ Database

MongoDB is deployed using the official Docker image within docker-compose.

---

## ☁️ Cloud Deployment

The application is deployed on an Ubuntu EC2 instance with:

- Docker
- Docker Compose
- Nginx reverse proxy

### Deployment Command

```
docker-compose up -d
```

---

## 🔄 CI/CD Pipeline

Implemented using GitHub Actions.

### Trigger
- Push to `main` branch

### Workflow Steps
1. Checkout repository
2. Login to Docker Hub
3. Build backend image
4. Build frontend image
5. Push images to Docker Hub

Workflow file location:

```
.github/workflows/deploy.yml
```

---

## 🌐 Reverse Proxy (Nginx)

Nginx is configured to:

- Route `/` → Frontend
- Route `/api/` → Backend
- Serve application on port 80

---

## 📸 Screenshots
![Uploading Screenshot 2026-02-24 204220.png…]()



- Docker Hub images
- CI/CD pipeline execution
- docker ps output
- Running application in browser
- Nginx configuration

---

## 📈 Key Learnings

- Docker image creation & multi-stage builds
- Multi-container orchestration with Docker Compose
- CI/CD automation using GitHub Actions
- Cloud deployment on AWS
- Reverse proxy configuration using Nginx

---

## 👤 Author

Durgansh
