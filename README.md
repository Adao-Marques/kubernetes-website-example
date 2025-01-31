# **Kubernetes Website Example**

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

This repository provides a **step-by-step guide** and Kubernetes manifests to deploy a simple website using **Nginx** as the web server and **MySQL** as the database. It covers key Kubernetes concepts like **Persistent Volumes**, **ConfigMaps**, **Deployments**, and **Services**. Perfect for learning Kubernetes or building production-ready applications.

---

## **Features**

- 🚀 **Nginx** as the web server.
- 🗃️ **MySQL** as the database with persistent storage.
- 📁 **Persistent Volume (PV)** and **Persistent Volume Claim (PVC)** for data persistence.
- 🛠️ **ConfigMap** for Nginx configuration.
- ⚙️ **Deployments** and **Services** for scalability and accessibility.
- 🌐 **NodePort** and **Port Forwarding** for external access.

---

## **Prerequisites**

Before you begin, ensure you have the following:

- A running Kubernetes cluster (e.g., [Minikube](https://minikube.sigs.k8s.io/docs/), [Kind](https://kind.sigs.k8s.io/), or a cloud provider like GKE, EKS, or AKS).
- `kubectl` installed and configured to interact with your cluster.
- Basic knowledge of Kubernetes concepts (Pods, Deployments, Services, etc.).

---

## **Quick Start**

1. Clone the repository:
   ```bash
   git clone https://github.com/Adao-Marques/kubernetes-website-example.git
   cd kubernetes-website-example

2. Apply the Kubernetes manifests:
   ```bash
   kubectl apply -f manifests/
3. Verify the resources:
   ```bash
   kubectl get all
4. Access the application:
  - Use NodePort or Port Forwarding to access the Nginx website.
  - Connect to MySQL using the mysql-service.

## **Manifests Overview**
The repository contains the following Kubernetes manifests:

Persistent Storage
  - manifests/persistent-volume.yaml: Persistent Volume for MySQL data.
  - manifests/persistent-volume-claim.yaml: Persistent Volume Claim for MySQL.

Nginx
  - manifests/nginx-configmap.yaml: ConfigMap for Nginx configuration.
  - manifests/nginx-deployment.yaml: Deployment for Nginx.
  - manifests/nginx-service.yaml: Service for Nginx (NodePort).

MySQL
  - manifests/mysql-deployment.yaml: Deployment for MySQL.
  - manifests/mysql-service.yaml: Service for MySQL (ClusterIP).
    
## **Accessing the Application**
Nginx Website
 - NodePort: Access the website using the NodePort assigned to the nginx-service:
   ```bash
   kubectl get services nginx-service
Example: http://<Node-IP>:<NodePort>
- Port Forwarding: Use kubectl port-forward for local access:

   ```bash
   kubectl port-forward service/nginx-service 8080:80
Access at: http://localhost:8080

MySQL Database
- Connect to MySQL internally using the mysql-service:
     ```bash
  kubectl run mysql-client --image=mysql:5.7 --rm -it --restart=Never -- \
    mysql -h mysql-service -u root -ppassword
---
Connect with Me

👨‍💻 GitHub: Adao-Marques | 
💼 LinkedIn: https://www.linkedin.com/in/ad%C3%A3o-marques/
