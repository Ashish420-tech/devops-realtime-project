# 🚀 DevOps Real-Time Project – Day 1 (Docker)

## 📌 Project Overview
This repository is part of a **real-time DevOps hands-on project** designed to follow **industry-standard DevOps practices**.

**Day-1 objective:**
- Build a simple web application
- Containerize the application using Docker
- Run and validate the application locally
- Prepare the project structure for Kubernetes deployment (next phase)

This reflects how applications are prepared in real organizations before CI/CD and Kubernetes deployment.

---

## 🧰 Tools & Technologies
- **Docker** – Containerization
- **Nginx** – Web server
- **HTML** – Sample application
- **Git & GitHub** – Version control
- **Linux (Ubuntu / WSL)** – Development environment

---

## 📂 Project Structure
devops-realtime-project/
├── app/
│ └── index.html
├── docker/
│ └── Dockerfile
├── k8s/
│ └── (Kubernetes manifests – upcoming)
└── README.md

yaml
Copy code

---

## 🧪 Application Description
A simple static HTML application served using **Nginx** inside a Docker container.

**Sample Output:**
Hello from DevOps Real Time Project 🚀
Docker + Kubernetes in action

yaml
Copy code

---

## 🐳 Docker Configuration

### Dockerfile
```dockerfile
FROM nginx:latest
COPY app/index.html /usr/share/nginx/html/index.html
🔨 Build Docker Image
Run the following command from the project root directory:

bash
Copy code
docker build -t devops-project:v1 -f docker/Dockerfile .
▶️ Run Docker Container
bash
Copy code
docker run -d -p 8081:80 devops-project:v1
🌐 Verify Application
Open your browser and access:

arduino
Copy code
http://localhost:8081
If the page loads successfully, the container is running correctly ✅

✅ Output
Docker image built successfully

Container running locally

Application served via Nginx

Real-world Docker issues (build context, port conflicts) handled

---

## ☸️ Day-2: Kubernetes Deployment

### Kubernetes Objects Used
- Deployment
- Service (NodePort)

### Apply Kubernetes Manifests
```bash
kubectl apply -f k8s/deployment.yml
kubectl apply -f k8s/service.yml
