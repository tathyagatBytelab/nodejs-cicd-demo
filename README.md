# 🚀 Node.js CI/CD Pipeline with Docker & GitHub Actions

This project was built as part of a DevOps internship task from **elevate Lab**, focused on implementing a full **CI/CD pipeline** using **GitHub Actions** and **DockerHub**.

---

## 🎯 Objective

To automate the process of building, testing, and deploying a Node.js web application using GitHub Actions. On every push to the `main` branch, the app is built as a Docker image and pushed to DockerHub.

---

## 🛠️ Tech Stack

- **Node.js** – Web application framework (Express)
- **Docker** – Containerization
- **GitHub Actions** – CI/CD pipeline
- **DockerHub** – Container image registry

---
## 🧱 Project Structure

```
nodejs-cicd-demo/
├── app.js # Express server code
├── package.json # App metadata and dependencies
├── Dockerfile # Container build instructions
└── .github/
└── workflows/
└── main.yml # CI/CD pipeline configuration

```
---

## 🔄 Step-by-Step Workflow

###  1. Project & Repo Setup
- Created GitHub repo: `nodejs-cicd-demo`
- Cloned it locally and initialized a basic Node.js app

###  2. Created Node.js App
- Used Express to create a simple server (`app.js`)
- Configured `package.json` and installed dependencies (`express`)

###  3. Dockerized the App
- Wrote a `Dockerfile` to:
  - Use Node base image
  - Copy app files
  - Install dependencies
  - Start the server
- Built and tested the image locally:
  ```bash
  docker build -t nodejs-cicd-demo .
  docker run -p 3000:3000 nodejs-cicd-demo

##  4. Created DockerHub Repo
 Created public repo: tathyagat/nodejs-cicd-demo

 Generated DockerHub access token for CI authentication

##  5. Set GitHub Secrets
DOCKER_USERNAME → tathyagat

DOCKER_PASSWORD → DockerHub access token

## 6. Created GitHub Actions Workflow
File: .github/workflows/main.yml

Steps:

Checkout code

Log in to DockerHub

Build Docker image

Push image to DockerHub
