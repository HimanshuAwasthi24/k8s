## Ingress
Is a method which helps in proccessing the requests to multiple services pods

## Ingress controller
Reads the ingress rules proccesses the requests to specific service

**Note: Minikube doesn't support ingress with docker driver, We need a linux vm.**

## Command to create minikube with vm driver
```bash
minikube start --vm=true -p ingress-cluster
```

### Steps to setup ingress
> Run Deployment file(kubectl apply -f deployment.yaml)</br>
> Run service file ()</br>
> Run kubernetes inbuilt ingress controller in minikube</br>
> minikube addons enable ingress -p cluster-profile</br>
> Verify ingress</br>
> kubectl get pods -n ingress-nginx