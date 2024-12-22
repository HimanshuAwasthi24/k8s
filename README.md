# k8s
Open source tool for container orchestration.

## architecture
![architecture](https://kubernetes.io/images/docs/kubernetes-cluster-architecture.svg "Optional Title")
## explanation of architecture
**control plane:** Is a node or machine that manages worker nodes, It also called master.</br>
**Nodes:** Worker nodes or data plane are the one on which the applications are running.

### control plane components

1. APi Server => All the communication via CLI or API or SDK is done by api server , Any components wants to communicate with eachother they use kube-apiserver, When a user provide commands using *kubectl* utility it first goes through api server in following ways.

> Authentication : If it's a valid user or not </br>
> Authoriaztion : Do you have permission to create resource </br>
> Admission : Validate, Mutate and reject request </br>

2. ETCD => It's a key-value storage which has every details about cluster and it's state, Every changes made by components in the cluster get's updated in ETCD by api-server. </br>

3. Scheduler => Helps to schedule to pods on various nodes based on resource utelization. </br>

4. kube-controller-manager => Maintains currecnt state to desired state , manages different controllers like replication controller, node controller, job controller etc. </br>

5. cloud controller manager =>  The cloud controller manager lets you link your cluster into your cloud provider's API,  If you are running Kubernetes on your own premises, or in a learning environment inside your own PC, the cluster does not have a cloud controller manager.</br>
*Example:*  Service controller: For creating, updating and deleting cloud provider load balancers</br>

6. kubelet => An agent that runs on each node in the cluster. It makes sure that containers are running in a Pod.</br>

7. Container runtime => A fundamental component that empowers Kubernetes to run containers effectively. It is responsible for managing the execution and lifecycle of containers within the Kubernetes environment.</br>
Kubernetes supports container runtimes such as containerd, CRI-O, and any other implementation of the Kubernetes CRI (Container Runtime Interface).</br>

8. kube-proxy => kube-proxy is a network proxy that runs on each node in your cluster, implementing part of the Kubernetes Service concept.</br>
kube-proxy maintains network rules on nodes. These network rules allow network communication to your Pods from network sessions inside or outside of your cluster.
