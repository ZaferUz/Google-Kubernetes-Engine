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
 - Node auto-repair to maintain node health and availability.
 - Cloud Logging and Monitoring for visibility into your cluster.
