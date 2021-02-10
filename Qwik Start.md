# Overview

- Google Kubernetes Engine (GKE) provides a managed environment for deploying, managing, and scaling your containerized applications using Google infrastructure. The GKE environment consists of multiple machines (specifically Google Compute Engine instances) grouped together to form a container cluster. In this lab, you will get hands on practice with container creation and application deployment with GKE.


## Cluster orchestration with GKE
- GKE clusters are powered by the Kubernetes open source cluster management system. Kubernetes provides the mechanisms through which you interact with your container cluster. You use Kubernetes commands and resources to deploy and manage your applications, perform administration tasks and set policies, and monitor the health of your deployed workloads.

- Kubernetes draws on the same design principles that run popular Google services and provides the same benefits: automatic management, monitoring and liveness probes for application containers, automatic scaling, rolling updates, and more. When you run your applications on a container cluster, you're using technology based on Google's 10+ years of experience running production workloads in containers.


## Kubernetes on Google Cloud
- When you run a GKE cluster, you also gain the benefit of advanced cluster management features that Google Cloud provides. These include:

  -Load-balancing for Compute Engine instances.
  -Node Pools to designate subsets of nodes within a cluster for additional flexibility.
  -Automatic scaling of your cluster's node instance count.
  -Automatic upgrades for your cluster's node software.
  -Node auto-repair to maintain node health and availability.
  -Cloud Logging and Monitoring for visibility into your cluster.
## Setup 
- You can list the active account name with this command:

```
gcloud auth list
```

- You can list the project ID with this command:
```
gcloud config list project

```

- set your default compute zone to us-central1-a:

```
gcloud config set compute/zone us-central1-a

```

## Creating a GKE cluster
```
gcloud container clusters create my-cluster

```
## Get authentication credentials for the cluster
- To authenticate the cluster run the following command, replacing [CLUSTER-NAME] with the name of your cluster:
```
gcloud container clusters get-credentials  my-cluster

```

## Deploying an application to the cluster
- Run the following kubectl run command in Cloud Shell to create a new Deployment hello-server from the hello-app container image:
```
kubectl create deployment hello-server --image=gcr.io/google-samples/hello-app:1.0

```

- create a Kubernetes Service, which is a Kubernetes resource that lets you expose your application to external traffic, by running the following kubectl expose command:
```
kubectl expose deployment hello-server --type="LoadBalancer" --port 8080

```

- Inspect the hello-server Service by running kubectl get

```
kubectl get service hello-server

```


- View the application from your web browser using the external IP address with the exposed port:

```
http://[EXTERNAL-IP]:8080

```
## Clean up

- Run the following to delete the cluster:
```
gcloud container clusters delete my-cluster
```



