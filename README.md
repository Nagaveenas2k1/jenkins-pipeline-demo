# jenkins-pipeline-demo

A simple Flask web app demonstrating a Jenkins CI/CD pipeline.

## Project Structure

- `app.py`: Flask app
- `requirements.txt`: Python dependencies
- `Dockerfile`: Containerizes app for consistent builds
- `Jenkinsfile`: Jenkins CI/CD Pipeline

## CI/CD Pipeline Steps

1. **Clone** the repository from GitHub.
2. **Build** a Docker image from source.
3. **Test** the running container (HTTP call).
4. **Deploy** step placeholder (customizable for cloud/server/registry).

## Setup Instructions

### Prerequisites

- **Docker** installed
- **Jenkins** (recommended: run in Docker)

### Running Jenkins Locally

- docker run -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts


### Running the App Locally

- docker build -t devops-demo-app:latest .
- docker run --rm -p 5000:5000 devops-demo-app:latest

Visit: [http://localhost:5000](http://localhost:5000)

---
