# k8s
Open source tool for container orchestration.

## architecture
![architecture](https://kubernetes.io/images/docs/kubernetes-cluster-architecture.svg "Optional Title")
## explanation of architecture
**control plane:** Is a node or machine that manages worker nodes, It also called master.
**Nodes:** Worker nodes or data plane are the one on which the applications are running.

### control plane components

1. APi Server => All the communication via CLI or API or SDK is done by api server , Any components wants to communicate with eachother they use kube-apiserver, When a user provide commands using *kubectl* utility it first goes through api server in following ways.

> Authentication : If it's a valid user or not
> Authoriaztion : Do you have permission to create resource
> Admission : Validate, Mutate and reject request