# MERN Stack Application Deployment on Minikube Kubernetes Cluster

This repository contains the necessary files and configurations to deploy a MERN (MongoDB, Express.js, React, Node.js) stack web application in a Minikube Kubernetes cluster using a CI/CD pipeline.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Deployment Files](#deployment-files)
- [Setup](#setup)
- [Configurations](#configurations)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before getting started, make sure you have the following installed:

- 💻 [Minikube] [Install Minikube](https://minikube.sigs.k8s.io/docs/start/)
- ☁️ [kubectl] [Install kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- 🐳 [Docker] [Install Docker](https://docs.docker.com/get-docker/)

## Deployment Files

- 🚀 **backend.yaml**: Kubernetes deployment and service configuration for the backend Node.js server.
- 🚀 **frontend.yaml**: Kubernetes deployment and service configuration for the frontend React application.
- 🚀 **mongodb.yaml**: Kubernetes deployment and service configuration for the MongoDB database.
- 🚀 **ingress.yaml**: Kubernetes ingress configuration for routing traffic to the frontend service.

## Setup

1. **Clone this repository:**
   ```bash
   git clone https://github.com/arunesh04/Kubenetes_Deploy-mern.git
   cd Kubenetes_Deploy-mern
   ```

2. **Set up Minikube:**
   ```bash
   minikube start  
   ```

3. **Set up Docker Environment:**
   ```bash
   eval $(minikube -p minikube docker-env)
   ```

4. **Apply Kubernetes manifests:**
   ```bash
   kubectl apply -f backend.yaml -f frontend.yaml -f mongodb.yaml -f ingress.yaml
   ```

5. **Access the application:**
   Once the application is deployed, you can access it by running:
   ```bash
   minikube service list
   ```

## Configurations

1. **Replace the port number assigned for MongoDB in the backend `connect.js` file.**

2. **Replace the port number assigned for the backend service in the frontend connection string.**

## Contributing

Feel free to contribute to this repository by creating pull requests. Suggestions, improvements, and bug fixes are always welcome!

## License

This project is licensed under the ![MIT License](https://img.shields.io/badge/License-MIT-blue). 
