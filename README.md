# Node.js CI/CD Pipeline with GitHub Actions & Docker

![CI Status](https://github.com/StrixPO/nodejs-cicd-pipeline/)  
![Docker Image](https://hub.docker.com/repository/docker/dockocto/nodejs-demo-app/general)

## Project Overview

This project demonstrates a simple **Node.js app** with a **CI/CD pipeline** powered by **GitHub Actions** and **Docker**. The goal is to automate the testing, building, and deployment of the Node.js application.

---

## Table of Contents

1. [Installation](#installation)
2. [Usage](#usage)
3. [CI/CD Pipeline](#cicd-pipeline)
4. [Docker Information](#docker-information)
5. [License](#license)

---

## Installation

### Prerequisites

- [Node.js](https://nodejs.org/) (version 20 or higher)
- [Docker](https://www.docker.com/) (optional for local testing)

### Steps to Set Up Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/StrixPO/nodejs-cicd-pipeline.git
   cd nodejs-cicd-pipeline
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

---

## Usage

To run the Node.js app locally:

1. Start the app:

   ```bash
   npm start
   ```

2. Open your browser and navigate to [http://localhost:3000](http://localhost:3000). You should see:
   ```
   Hello from Node.js demo app!
   ```

---

## CI/CD Pipeline

### GitHub Actions Workflow

This repository uses **GitHub Actions** to automate the CI/CD pipeline. The pipeline consists of:

- **Install dependencies** using `npm install`.
- **Run tests** (currently a dummy test).
- **Build Docker image** using the `Dockerfile`.
- **Push the Docker image** to DockerHub.

The pipeline is triggered on every **push to the `main` branch**.

You can monitor the status of the CI/CD pipeline by visiting the **Actions** tab in the GitHub repository.

---

## Docker Information

### Build and Run Locally (Optional)

If you have Docker installed, you can build and run the Docker container locally:

1. Build the Docker image:

   ```bash
   docker build -t nodejs-demo-app .
   ```

2. Run the Docker container:

   ```bash
   docker run -p 3000:3000 nodejs-demo-app
   ```

3. Open your browser and visit [http://localhost:3000](http://localhost:3000) to view the app.

### DockerHub

The Docker image for this project is pushed to DockerHub under the repository:  
`YOUR_DOCKER_USERNAME/nodejs-demo-app:latest`

You can pull the image from DockerHub with:

```bash
docker pull dockocto/nodejs-demo-app:latest
```
