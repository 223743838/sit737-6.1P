6.1P Task

This project demonstrates deploying a simple Node.js-based video streaming microservice using Docker and Kubernetes.

Project Structure ├── Dockerfile-prod # Production-ready Dockerfile ├── src/ │ └── index.js # Node.js entrypoint ├── scripts/ │ └── deploy.yaml # Kubernetes deployment and service YAML ├── package.json ├── README.md #

Steps to Run

Build Docker Image
Make sure you're in the project root directory, then run:

docker build -t imagename:1 -f Dockerfile-prod .

Test Docker Image Locally (optional)

docker run -p 4000:4000 imagename:1

3. Deploy to Kubernetes
Ensure your Kubernetes cluster is running (e.g., via Docker Desktop), then run:

kubectl apply -f scripts/deploy.yaml
Check resources:

kubectl get pods
kubectl get deployments
kubectl get services
4. Access the Service
Find the NodePort (default is 30000 from deploy.yaml):

Author 

Sushma Singh
223743838