# Orange-Kubernetes-Project


Here’s a sample README file for your Kubernetes project:

---

# Kubernetes Multi-Tier Application Project

## Project Overview

This project sets up a multi-tier application architecture using Kubernetes, consisting of three main components: 
- **Proxy Tier** (Nginx)
- **Backend Tier** (Go application)
- **Database Tier** (MySQL)

Each tier is deployed as a Kubernetes Deployment with 2 replicas for high availability, and they communicate with each other through Kubernetes Services. The database credentials are securely mounted in the respective pods.

## Kubernetes Resources

### Deployments
- **Backend Deployment (`backend_deployment.yaml`)**: Defines the Go backend service with 2 replicas.
- **Database Deployment (`database_deployment.yaml`)**: Defines the MySQL database with 2 replicas.
- **Proxy Deployment (`proxy_deployment.yaml`)**: Nginx proxy service with 2 replicas.

### Services
- **Backend Service (`backend_service.yaml`)**: Exposes the backend internally within the cluster.
- **Database Service (`db_service.yaml`)**: Cluster-internal service for the MySQL database.
- **Proxy Service (`proxy_nodeport.yaml`)**: Exposes the Nginx proxy externally using a NodePort.

### Volumes
- **Persistent Volume (`db-data-pv.yaml`)**: Defines a PersistentVolume for MySQL data storage.
- **Persistent Volume Claim (`db-data-pvc.yaml`)**: Requests storage for MySQL from the PersistentVolume.
- **Secret (`db-secret.yaml`)**: Stores MySQL database credentials and mounts them securely into the database pod.

## Project Output


!(.)[https://github.com/SaifmElnagar/Orange-Kubernetes-Project/blob/main/Screenshot%20from%202024-09-20%2018-56-18.png]






