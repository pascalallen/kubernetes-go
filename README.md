# kubernetes-go

kubernetes-go is a Go module that offers tools to deploy to Kubernetes. There is a publication for this repository which can be found [here](https://pascalallen.medium.com/how-to-deploy-to-kubernetes-76c42e5ea28c).

## Prerequisites

- [Docker](https://www.docker.com/)
- [Kubernetes](https://kubernetes.io/releases/download/)
- [kubectl](https://kubernetes.io/releases/download/)
- [A Docker Hub account](https://hub.docker.com/)

## Kubernetes Deployment Steps

### Build and Tag Docker Image

```bash
docker build -t pascalallen/kubernetes-go .
```

### Log in to Docker Hub

```bash
docker login
```

### Push Image to Docker Hub

```bash
docker push pascalallen/kubernetes-go
``` 

### Apply Service to Kubernetes Cluster

```bash
kubectl apply -f etc/k8s/go
```

Locally, you will find the site running at http://localhost:9990/

### List Kubernetes Pods

```bash
kubectl get pods
```

### List Kubernetes Services

```bash
kubectl get services
```

### Delete Service and Pod from Kubernetes Cluster

```bash
kubectl delete -f etc/k8s/go
```

