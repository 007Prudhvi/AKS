# AKS Components

## Table of Contents

- Azure Managed
  - [control plane](#control-plane)
  - [kube-apiserver](#kube-apiserver)
  - [kube-apiserver](#kube-apiserver)
  - [kube-controller-manager](#kube-controller-manager)
  - [kube-scheduler](#kube-scheduler)
  - [etcd](#etcd)
- Customer Managed
  - [kubelet](#kubelet)
  - [kube-proxy](#kube-proxy)
  - [container runtime](#container-runtime)
  - [container](#container)

## Azure Managed

### control plane

The control plane is a set of processes that control the Kubernetes cluster. It is responsible for maintaining the desired state of the cluster, such as which applications are running and which container images they use. It also handles scheduling and scaling of applications across the cluster.

### kube-apiserver

The kube-apiserver is the front-end for the Kubernetes API. It exposes the Kubernetes API, which is used by other components to communicate with the cluster. It also handles authentication and authorization of requests to the API.

### kube-controller-manager

The kube-controller-manager is responsible for maintaining the desired state of the cluster. It watches the state of the cluster and makes changes to bring it back into the desired state. It also handles scheduling and scaling of applications across the cluster.

### kube-scheduler

The kube-scheduler is responsible for scheduling applications across the cluster. It watches the state of the cluster and makes decisions about where to place applications based on resource requirements, affinity rules, and other factors.

### etcd

etcd is a distributed key-value store that is used by Kubernetes to store cluster state. It is a highly available, fault-tolerant, and consistent data store that is used by Kubernetes to store cluster state.

## Customer Managed

### kubelet

The kubelet is responsible for running containers on a node. It is responsible for starting, stopping, and monitoring containers on a node. It also handles logging and monitoring of containers on a node.

### kube-proxy

The kube-proxy is responsible for routing traffic to containers on a node. It is responsible for routing traffic to containers on a node. It also handles load balancing of traffic across containers on a node.

### container runtime

The container runtime is responsible for running containers on a node. It is responsible for starting, stopping, and monitoring containers on a node. It also handles logging and monitoring of containers on a node.

### container

A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another.

## References

- [Kubernetes Components](https://kubernetes.io/docs/concepts/overview/components/)
