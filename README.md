Dockerized Full-Stack Notes Application

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)

## 📌 Project Overview
This repository demonstrates the end-to-end containerization of a multi-tier web application. The primary objective of this project was to take an existing application and design a modern, isolated infrastructure environment using Docker and Docker Compose.

**Infrastructure & DevOps Implementation:**
While the base Python/React application code was originally authored by [Shubham Londhe](https://github.com/LondheShubham153), my technical focus for this repository was entirely on the **DevOps and deployment tier**. I reverse-engineered the application's dependencies to build a reliable, fully containerized local development environment.

## 🏗️ Architecture & Features
* **Multi-Container Orchestration:** Utilized `docker-compose.yml` to bridge the frontend and backend networks seamlessly.
* **Custom Dockerfiles:** Engineered distinct, optimized images for both the Django (Python) backend and the React (Node.js) frontend.
* **Reverse Proxy:** Configured Nginx to route traffic, handle static files, and serve as the entry point for the application.
* **Volume Management:** Implemented Docker volumes to ensure database persistence across container restarts.

## 🚀 Local Setup & Installation

### Prerequisites
* [Docker](https://www.docker.com/get-started) installed and running.
* Docker Compose.
* Git.

### Step-by-Step Deployment

**1. Clone the repository:**
```bash
git clone [https://github.com/sudarshanvashisht/django-notes-app.git](https://github.com/sudarshanvashisht/django-notes-app.git)
cd django-notes-app
2. Build and spin up the environment:

Bash
docker-compose up -d --build
(The -d flag runs the containers in the background, keeping your terminal free).

3. Access the application:

Frontend Client: http://localhost:80 (or the port defined in your configuration)

Backend API/Admin: http://localhost:8000

4. Shut down the environment:

Bash
docker-compose down
📂 Infrastructure Directory Structure
Plaintext
📦 django-notes-app
 ┣ 📂 api/                # Django Backend Application
 ┣ 📂 mynotes/            # React Frontend Application
 ┣ 📂 nginx/              # Nginx Configuration
 │ ┣ 📜 Dockerfile        # Nginx Container Build
 │ ┗ 📜 default.conf      # Proxy Routing Rules
 ┣ 📜 Dockerfile          # Django Container Build
 ┣ 📜 docker-compose.yml  # Multi-container Orchestration
 ┗ 📜 requirements.txt    # Python Dependencies
👨‍💻 About the Developer
Sudarshan Vashisht

B.Tech Computer Science and Engineering student focused on software infrastructure, deployment architecture, and full-stack development.

