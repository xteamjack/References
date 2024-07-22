# Installation on Windows

## Step 1 - Setup Cluster
Cluster is to create a Kubernetes cluster in one of the following options
1. With Docker Desktop
2. Minikube
3. Microk8s

### Kubernetes on Docker Desktop
One of the easiest approach, go to setting in Docker Desktop and select option run kubernetes

## Step 2 - Setup kubectl

## Step 3 - Test the cluster

```
kubectl version

kubectl cluster-info

kubectl config get-contexts

kubectl config current-context
```

## Step 4 - Configure kubectl

```
kubectl config use-context docker-desktop
```

## Step 5 - Configure Dashboard
An easy way to access kubernetes info

## Step 6 - Configure Local Docker Repo
Kubernetes access images from a docker repo. You can configure an external repo like docker hub, azure repo etc., or configure a local repository.

Local repo inside a network is ideal for development and testing while integrated with CI CD pipeline
