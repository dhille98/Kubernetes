# Kubernetes

## Installing nginx ingress controller

```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/cloud/deploy.yaml
```
### Steps to Install NGINX Ingress Controller
**Create a Namespace:**
First, create a namespace for the NGINX Ingress Controller:
```bash
kubectl create namespace ingress-nginx
```
**Apply the NGINX Ingress Controller Manifest:**
Use the following command to deploy the NGINX Ingress Controller by applying the official manifest:
```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/cloud/deploy.yaml
```
**Verify the Deployment:**
Check that the NGINX Ingress Controller pods are running:
```bash
kubectl get pods --namespace ingress-nginx
```
**Check the Service:**
To see if the NGINX Ingress Controller has been assigned a public IP address, run:
```bash
kubectl get svc --namespace ingress-nginx
```
Look for the service of type LoadBalancer and note its EXTERNAL-IP. It may take a few minutes for the IP to be assigned.
**Troubleshooting:**
If the EXTERNAL-IP status shows as Pending, you can investigate further with:
```bash
kubectl describe svc -n ingress-nginx ingress-nginx-controller
```