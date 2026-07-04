# i2i Academy - Containerization & Cloud Deployment Homework

This repository contains the configuration files for containerizing a static web page using Docker Compose and deploying it both locally and on Google Cloud Platform (GCP).

## Project Structure
* `index.html`: The custom HTML page served by Nginx.
* `docker-compose.yml`: The Docker Compose configuration that orchestrates the Nginx container.

## Deployment Steps

### 1. Local Deployment
To run this project on your local machine, navigate to the project directory and execute:
```bash
docker compose up -d
Once started, the application will be available at http://localhost:8080

2. Cloud Deployment (GCP)
To deploy the application on a Google Cloud VM instance:

SSH into your GCP VM instance.

Install Docker and Docker Compose:

Bash
sudo apt update && sudo apt install docker.io docker-compose-v2 -y
Create the project files (docker-compose.yml and index.html) on the server.

Start the container in detached mode:

Bash
sudo docker compose up -d
Ensure that a GCP Firewall rule is created to allow incoming ingress traffic on port 8080.

Access the web server using your VM's External IP: http://<VM_EXTERNAL_IP>:8080.