# Requirements

> 2 CPUs or more</br>
>  2GB of free memory</br>
> 20GB of free disk space</br>
> Internet connection</br>
> Container or virtual machine manager, such as: Docker, QEMU, Hyperkit, Hyper-V, KVM, Parallels, Podman, VirtualBox, or VMware Fusion/Workstation

# Download minikube binary for linux
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64

#start cluster
minikube start --nodes NumbeOfNodes -p profileName --driver=docker

```