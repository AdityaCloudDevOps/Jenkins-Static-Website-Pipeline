# Jenkins CI/CD Pipeline with Docker Deployment

## Project Overview

This project demonstrates a real-time CI/CD pipeline using Jenkins, Docker, GitHub, and Ubuntu Linux.

The pipeline automatically builds and deploys a containerized Gym/Fitness website whenever code changes are pushed to GitHub.

---

# Tech Stack

- Jenkins
- Docker
- GitHub
- Ubuntu Linux
- HTML
- CSS
- Nginx

---

# Project Architecture

Developer → GitHub → Jenkins Pipeline → Docker Build → Container Deployment → Live Website

---

# CI/CD Workflow

1. Developer pushes code to GitHub
2. Jenkins scheduler checks repository changes
3. Jenkins pipeline starts automatically
4. Docker image is built
5. Old container is removed
6. New container is deployed
7. Updated website becomes live

---

# Jenkins Scheduler

The pipeline uses CRON scheduling:

```groovy
triggers {
    cron('H/2 * * * *')
}
```

This checks for changes every 2 minutes.

---

# Docker Usage

Docker is used for:
- Containerized deployment
- Consistent runtime environment
- Lightweight web hosting
- Application portability

---

# Docker Commands Used

## Build Image

```bash
docker build -t devops-website .
```

## Run Container

```bash
docker run -d -p 80:80 --name devops-container devops-website
```

## Check Running Containers

```bash
docker ps
```

---

# Jenkins Pipeline Stages

## Build Docker Image
Builds the application image using Dockerfile.

## Stop Old Container
Removes previously running container.

## Run New Container
Deploys latest application version.

---

# Features

- Automated CI/CD Pipeline
- Docker-based deployment
- Jenkins scheduler automation
- GitHub integration
- Real-time deployment workflow
- Production-style deployment architecture

---

# Learning Outcomes

- Jenkins Pipeline
- CI/CD Concepts
- Docker Containerization
- GitHub Integration
- Linux Administration
- Deployment Automation
- Infrastructure Automation

---

# Screenshots

## Jenkins Pipeline Success

(Add Screenshot)

## Docker Running Container

(Add Screenshot)

## Live Website

(Add Screenshot)

---

# Author

Aditya Yadav