# 🚀 Flask Portfolio – CI/CD Deployment with Docker & AWS

A personal portfolio web application built using **Flask**, containerized with **Docker**, and deployed to the cloud using **AWS EC2** with a complete **CI/CD pipeline using GitHub Actions**.

The project demonstrates how modern DevOps workflows automate building, packaging, and deploying applications.

---

# 🌐 Live Demo

🔗 **Live Application:**
http://13.205.253.79:5000

The application is hosted on **AWS EC2** and automatically updates whenever new code is pushed to GitHub.

---

# 🧠 Project Goal

The main objective of this project was to learn and implement:

* Docker containerization
* CI/CD automation
* Cloud deployment
* Automated application updates
* DevOps workflow using modern tools

---

# ⚙️ Tech Stack

| Technology     | Purpose                     |
| -------------- | --------------------------- |
| Python         | Backend programming         |
| Flask          | Web framework               |
| HTML / CSS     | Frontend                    |
| Docker         | Containerization            |
| GitHub         | Code repository             |
| GitHub Actions | CI/CD pipeline              |
| Docker Hub     | Container registry          |
| AWS EC2        | Cloud hosting               |
| Watchtower     | Automatic container updates |

---

# 🏗️ Project Architecture

The deployment pipeline follows this flow:

```
Developer
   ↓
GitHub Repository
   ↓
GitHub Actions CI/CD
   ↓
Docker Image Build
   ↓
Push Image to Docker Hub
   ↓
AWS EC2 Server
   ↓
Watchtower detects update
   ↓
Automatic container restart
   ↓
Live Website Updated
```

---

# 📂 Project Structure

```
Portfolio/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── .dockerignore
├── .gitignore
│
├── templates/
│   └── index.html
│
├── static/
│   └── styles.css
│
└── .github/
    └── workflows/
        └── ci-cd.yml
```

---

# 🐳 Docker Containerization

The application was containerized using Docker.

### Dockerfile Responsibilities

The Dockerfile:

* Uses a Python base image
* Installs dependencies
* Copies the application code
* Runs the Flask application

This allows the application to run consistently on any system that supports Docker.

---

# 🔄 CI/CD Pipeline

A CI/CD workflow was created using **GitHub Actions**.

Whenever code is pushed to the repository:

1. GitHub Actions automatically starts
2. Docker image is built
3. Image is pushed to Docker Hub
4. EC2 server detects the new image
5. Watchtower pulls the new image
6. The running container updates automatically

This removes the need for manual deployment.

---

# ☁️ Cloud Deployment (AWS EC2)

The application is deployed on an **AWS EC2 Ubuntu server**.

Steps performed:

1. Launch EC2 instance
2. Create SSH key pair (`.pem`) for secure access
3. Connect to the instance via SSH
4. Install Docker on the server
5. Pull the Docker image from Docker Hub
6. Run the container on port **5000**

---

# 🔑 Elastic IP

An **Elastic IP** was attached to the EC2 instance so that the public address remains constant even after server restarts.

This provides a stable link for the live application.

---

# 🤖 Automatic Updates with Watchtower

Watchtower was deployed as a Docker container on the server.

Its role:

* Periodically check Docker Hub for new images
* Pull updated images automatically
* Restart containers with the new version

This enables **fully automated deployments**.



---

# 📚 What I Learned

Through this project I learned how to:

* Build a Flask web application
* Containerize applications using Docker
* Create CI/CD pipelines with GitHub Actions
* Push and manage Docker images on Docker Hub
* Deploy applications on AWS EC2
* Use SSH and key pairs for secure server access
* Implement automated container updates with Watchtower
* Understand real-world DevOps deployment workflows


---

