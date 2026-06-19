# Docker Compose Multi-Container Application

A containerized three-tier web application built using Docker Compose. The project demonstrates how multiple services can be deployed, networked, and managed together using a single Compose configuration.

## Architecture

The application consists of three services:

* **Frontend:** Nginx
* **Backend:** Flask (Python)
* **Database:** MySQL 8

Each service runs in its own container and communicates through a Docker Compose managed network.

## Features

* Multi-container deployment with Docker Compose
* Service-to-service communication using Docker networking
* Environment variable management with `.env`
* Persistent database storage using Docker volumes
* Backend service scaling
* Isolated application network

## Project Structure

```text
.
├── backend/
│   ├── app.py
│   ├── requirements.txt
│   └── Dockerfile
│
├── frontend/
│   ├── index.html
│   └── Dockerfile
│
├── docker-compose.yml
├── .env.example
└── README.md
```

## Technologies Used

* Docker
* Docker Compose
* Python
* Flask
* MySQL
* Nginx

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/tanvirdsingh/docker-compose-multi-container-app.git
cd docker-compose-multi-container-app
```

### Configure Environment Variables

Create a `.env` file using the provided example:

```bash
cp .env.example .env
```

### Build and Start the Application

```bash
docker compose up -d --build
```

### Verify Running Services

```bash
docker compose ps
```

### Stop the Application

```bash
docker compose down
```

## Scaling the Backend

Docker Compose allows horizontal scaling of the backend service.

```bash
docker compose up -d --scale backend=3
```

This creates multiple backend containers while maintaining communication through the Compose network.

## Key Concepts Demonstrated

* Containerization
* Service Discovery
* Docker Networking
* Persistent Volumes
* Environment Variables
* Multi-Service Application Deployment
* Horizontal Scaling

## Future Improvements

* Add a reverse proxy configuration
* Implement health checks
* Add monitoring and logging
* Deploy using Kubernetes
* Integrate CI/CD pipelines

## Author

**Tanvir Singh Dhillon**

RHCSA Certified | Linux & Cloud Enthusiast

LinkedIn: www.linkedin.com/in/tanvir-singh-dhillon-4960a53a5

