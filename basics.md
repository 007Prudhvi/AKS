# Azure Kubernetes Service

## Table of Contents

- [Basics](#basics)
  - [What is Kubernetes?](#what-is-kubernetes)
  - [What is Azure Kubernetes Service?](#what-is-azure-kubernetes-service)
  - [What is a Container?](#what-is-a-container)
  - [What is a Pod?](#what-is-a-pod)
  - [What is a Service?](#what-is-a-service)
  - [What is a Deployment?](#what-is-a-deployment)
  - [What is a ReplicaSet?](#what-is-a-replicaset)
  - [What is a Namespace?](#what-is-a-namespace)
  - [What is a Node?](#what-is-a-node)
  - [What is a Cluster?](#what-is-a-cluster)
  - [What is a Container Registry?](#what-is-a-container-registry)
  - [What is a Container Image?](#what-is-a-container-image)
  - [What is a Container Runtime?](#what-is-a-container-runtime)
  - [What is a Container Orchestration?](#what-is-a-container-orchestration)
  - [What is a Container Orchestration System?](#what-is-a-container-orchestration-system)
  - [What is a Container Orchestration Platform?](#what-is-a-container-orchestration-platform)

## Basics

### What is Kubernetes?

Kubernetes is an open-source container orchestration system for automating application deployment, scaling, and management. It was originally designed by Google and is now maintained by the Cloud Native Computing Foundation.

### What is Azure Kubernetes Service?

Azure Kubernetes Service (AKS) is a managed container orchestration service, based on the open source Kubernetes system, which is available on the Microsoft Azure public cloud.

### What is a Container?

A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another.

### What is a Pod?

A pod is the smallest deployable unit of computing that can be created and managed in Kubernetes. A pod consists of one or more containers that are guaranteed to be co-located on the host machine and can share resources.

### What is a Service?

A service is an abstraction which defines a logical set of pods and a policy by which to access them. Services enable a loose coupling between dependent pods. A service is defined using YAML (preferred) or JSON, like all Kubernetes objects.

### What is a Deployment?

A deployment is a Kubernetes object that allows you to specify the desired state of your application. It allows you to deploy multiple replicas of your application and scale it up or down as needed.

### What is a ReplicaSet?

A ReplicaSet is a Kubernetes object that allows you to specify the desired state of your application. A ReplicaSet in Kubernetes is a fundamental concept that is used to ensure the desired number of "replica" pods are always running in a cluster.

The "desired state" mentioned here refers to the number of instances (replicas) of a particular application that you want to be running at any given time. This could be any number, depending on the load that the application is expected to handle.

The ReplicaSet constantly monitors the number of running pods and compares it with the desired state. If there are too many pods, it will terminate the extra ones; if there are too few, it will start more.

The ability to "scale up or down as needed" means that you can increase or decrease the number of running instances of your application based on the demand or load. This is a crucial feature for applications that need to handle varying loads at different times.

In summary, a ReplicaSet in Kubernetes is a way to manage the lifecycle of pods and ensure that your application is running the desired number of instances at all times.

### What is a Namespace?

A namespace is a Kubernetes object that allows you to group resources together. It is a way to divide cluster resources between multiple users (via resource quota).

### What is a Node?

A node is a worker machine in Kubernetes. It may be a VM or physical machine, depending on the cluster. Each node has the services necessary to run pods and is managed by the master components.

### What is a Cluster?

A cluster is a set of nodes grouped together. A cluster consists of at least one master node and one or more worker nodes.

### What is a Container Registry?

A container registry is a service that stores container images. It is used to store and distribute container images.

### What is a Container Image?

A container image is a file that contains all the files necessary to run a container. It is used to create containers.

### What is a Container Runtime?

A container runtime is a software that runs containers. It is used to run containers.

### What is a Container Orchestration?

Container orchestration is the process of managing the lifecycle of containers. It is used to manage containers.

### What is a Container Orchestration System?

A container orchestration system is a software that manages containers. It is used to manage containers.

##References

- [Kubernetes Concepts](https://kubernetes.io/docs/concepts/)

### Types of Kubernetes Services?

There are five types of Services:

**ClusterIP (default):** Internal clients send requests to a stable internal IP address.

**NodePort:** Clients send requests to the IP address of a node on one or more `nodePort` values that are specified by the Service.

**LoadBalancer:** Clients send requests to the IP address of a network load balancer.

**ExternalName:** Internal clients use the DNS name of a Service as an alias for an external DNS name.

**Headless:** You can use a headless service when you want a Pod grouping, but don't need a stable IP address.

The `NodePort` type is an extension of the `ClusterIP` type. So a Service of type `NodePort` has a cluster IP address.

The `LoadBalancer` type is an extension of the `NodePort` type. So a Service of type `LoadBalancer` has a cluster IP address and one or more `nodePort` values.