# Shortlinks App

This project is a simple 2-layer application consisting of a backend (server) and a frontend (client). The frontend is built with **React**, and the backend is built with **Node.js**. It is designed to be easily deployed using either Kubernetes (K8s) or Docker Compose.

## Project Structure

- **client/**: React-based frontend application for interacting with the shortlinks service.
- **server/**: Node.js/Express backend providing API endpoints and business logic.

## Deployment Options

### 1. Docker Compose

You can run both the backend and frontend locally using Docker Compose. Use the provided `docker-compose.yml` file to spin up the services:

```sh
docker-compose up --build
```

### 2. Kubernetes

The project includes Kubernetes manifests for deploying the application to a K8s cluster:
- `deployment.yaml`: Deploys the backend and frontend pods.
- `service-lb-test.yaml`, `service-nodeport-test.yaml`: Service definitions for exposing the applications.
- `ingress.yaml`: Ingress configuration for routing external traffic.
- `certificate-test.yaml`: Example certificate configuration (if needed).

Apply the manifests using:

```sh
kubectl apply -f deployment.yaml
kubectl apply -f service-lb-test.yaml
kubectl apply -f service-nodeport-test.yaml
kubectl apply -f ingress.yaml
kubectl apply -f certificate-test.yaml
```

## Features
- Shorten and manage links via a simple web interface.
- User authentication and link management.
- Easily switch between local (Docker Compose) and cloud-native (Kubernetes) deployments.

## Prerequisites
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- [Kubernetes](https://kubernetes.io/) (for K8s deployment)

## Getting Started
See the `client/README.md` for frontend details and `server/` for backend configuration.

---

Feel free to customize the deployment files as needed for your environment.
