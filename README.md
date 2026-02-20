# Kubernetes home lab (kind)

Small lab to practice basic Kubernetes concepts using kind (Kubernetes in Docker).

## What I did
- Created a local Kubernetes cluster with kind
- Deployed an nginx app using YAML (Deployment + Service)
- Checked pods and basic troubleshooting with kubectl (get, describe, logs)
- Tested access using port forward

## How to run
Prereqs: Docker, kubectl, kind

```bash
kind create cluster --name lab
kubectl apply -f k8s/
kubectl get pods
kubectl port-forward svc/nginx-web-svc 8080:80
curl -I http://127.0.0.1:8080
