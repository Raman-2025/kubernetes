# Kubernetes Practice Notes

This repository contains my Kubernetes learning and practice files.

## What I Learned

* Kubernetes Architecture
* Kind Cluster
* Minikube
* Pods
* Namespaces
* Labels and Selectors
* Deployments
* ReplicaSets
* Services
* ConfigMaps
* Secrets
* Volumes
* Persistent Volumes (PV)
* Persistent Volume Claims (PVC)
* Ingress
* Helm
* Sidecar Containers
* Init Containers
* Monitoring Basics
* Troubleshooting

---

## Create Kind Cluster

```bash
kind create cluster --name tws-cluster
```

Check cluster:

```bash
kubectl get nodes
```

Delete cluster:

```bash
kind delete cluster --name tws-cluster
```

---

## Start Minikube

```bash
minikube start
```

Check status:

```bash
minikube status
```

---

## Namespace

Create namespace:

```bash
kubectl create namespace dev
```

View namespaces:

```bash
kubectl get ns
```

---

## Pods

Create pod:

```bash
kubectl run nginx --image=nginx
```

View pods:

```bash
kubectl get pods
```

Pod details:

```bash
kubectl describe pod nginx
```

Logs:

```bash
kubectl logs nginx
```

---

## Deployments

Create deployment:

```bash
kubectl apply -f deployment.yml
```

View deployments:

```bash
kubectl get deployments
```

Scale deployment:

```bash
kubectl scale deployment nginx-deployment --replicas=3
```

---

## Services

Create service:

```bash
kubectl apply -f service.yml
```

View services:

```bash
kubectl get svc
```

---

## ConfigMaps and Secrets

Create ConfigMap:

```bash
kubectl create configmap app-config --from-file=config.properties
```

Create Secret:

```bash
kubectl create secret generic app-secret --from-literal=password=admin123
```

---

## Storage

Create Persistent Volume:

```bash
kubectl apply -f pv.yml
```

Create Persistent Volume Claim:

```bash
kubectl apply -f pvc.yml
```

Check storage:

```bash
kubectl get pv
kubectl get pvc
```

---

## Ingress

Enable ingress in Minikube:

```bash
minikube addons enable ingress
```

Apply ingress:

```bash
kubectl apply -f ingress.yml
```

Check ingress:

```bash
kubectl get ingress
```

---

## Helm

Create chart:

```bash
helm create my-chart
```

Install chart:

```bash
helm install my-app my-chart
```

View releases:

```bash
helm list
```

Uninstall chart:

```bash
helm uninstall my-app
```

---

## Sidecar Container

Apply sidecar pod:

```bash
kubectl apply -f sidecar-container.yml
```

---

## Init Container

Apply init container:

```bash
kubectl apply -f init-container.yml
```

---

## Monitoring

Install Metrics Server:

```bash
kubectl top nodes
kubectl top pods
```

Install Prometheus and Grafana using Helm.

---

## Troubleshooting Commands

Check cluster:

```bash
kubectl get nodes
```

Check pods:

```bash
kubectl get pods -A
```

Describe pod:

```bash
kubectl describe pod <pod-name>
```

View logs:

```bash
kubectl logs <pod-name>
```

Access container:

```bash
kubectl exec -it <pod-name> -- sh
```

Check events:

```bash
kubectl get events
```

---

## Learning Projects

* Nginx Application Deployment
* Notes App Deployment
* Chat Application Deployment
* Helm Chart Deployment
* Monitoring with Prometheus and Grafana
* Ingress Setup
* Multi-Container Pod Practice

---

## Goal

Learn Kubernetes fundamentals through hands-on practice and build confidence in deploying, managing, and troubleshooting containerized applications.

