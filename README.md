# Jenkins Demo App 2025

A simple **CI/CD demo** showing how to build and deploy a containerized application with **Jenkins** and **Docker**.

This repository contains:
* `Jenkinsfile` – Declarative pipeline definition for automated build & deploy.
* Application source code (sample web app – edit as needed).
* `Dockerfile` – Instructions to build a lightweight container image.

---

## 🚀 Features
- **Continuous Integration**: Automatically builds a Docker image on each commit.
- **Continuous Delivery/Deployment**: Runs the container and exposes it on port `8080`.
- **Error Handling**: Includes basic try/catch and `post` steps for notifications.

---

## 📂 Project Structure

├── Dockerfile
├── Jenkinsfile
├── app/ # Your application code
└── README.md



## 🛠️ Prerequisites
* [Docker](https://docs.docker.com/get-docker/)
* [Jenkins](https://www.jenkins.io/download/)
    * Pipeline and Git plugins enabled
* GitHub repository webhook (optional for auto-trigger)

---

## ⚙️ Setup & Run

1. Clone the Repo
```bash
git clone https://github.com/madhugundarapu/jenkins-demo-app2025.git
cd jenkins-demo-app2025
2. Configure Jenkins

Create a Pipeline job in Jenkins.

Under “Pipeline → Definition”, choose Pipeline script from SCM.

SCM: Git → URL: https://github.com/madhugundarapu/jenkins-demo-app2025.git.

Branch: main (or your branch).

3. Build & Deploy

Click Build Now to start the pipeline.

Jenkins will:

Checkout the code

Build the Docker image: docker build -t demo-app .

Run the container: docker run -d -p 4000:8080 --name demo-app demo-app

 Test Locally (Optional)
docker build -t demo-app .
docker run -d -p 8080:8080 demo-app

Open http://localhost:4000
 to view the app.

🧹 Cleanup
docker stop demo-app
docker rm demo-app
docker rmi demo-app
