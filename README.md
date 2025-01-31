# kubernetes-website-example
This repository provides a step-by-step guide and Kubernetes manifests to deploy a simple website using Nginx as the web server and MySQL as the database. It covers key Kubernetes concepts like Persistent Volumes, ConfigMaps, Deployments, and Services. Perfect for learning Kubernetes or building production-ready applications.
Features
🚀 Nginx as the web server.

🗃️ MySQL as the database with persistent storage.

📁 Persistent Volume (PV) and Persistent Volume Claim (PVC) for data persistence.

🛠️ ConfigMap for Nginx configuration.

⚙️ Deployments and Services for scalability and accessibility.

Prerequisites
A running Kubernetes cluster (e.g., Minikube, Kind, GKE, EKS, or AKS).

kubectl installed and configured.

Quick Start
Clone the repository:

bash
Copy
git clone https://github.com/Adao-Marques/kubernetes-website-example.git
cd kubernetes-website-example
Apply the Kubernetes manifests:

bash
Copy
kubectl apply -f manifests/
Access the application:

Use NodePort or kubectl port-forward to access the Nginx website.

Connect to MySQL using the mysql-service.

Manifests Overview
manifests/persistent-volume.yaml: Persistent Volume for MySQL data.

manifests/persistent-volume-claim.yaml: Persistent Volume Claim for MySQL.

manifests/nginx-configmap.yaml: ConfigMap for Nginx configuration.

manifests/nginx-deployment.yaml: Deployment for Nginx.

manifests/nginx-service.yaml: Service for Nginx.

manifests/mysql-deployment.yaml: Deployment for MySQL.

manifests/mysql-service.yaml: Service for MySQL.

Accessing the Application
Nginx Website: Access via NodePort or kubectl port-forward.

MySQL Database: Connect internally using the mysql-service.

Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

License
This project is licensed under the MIT License. See the LICENSE file for details.
