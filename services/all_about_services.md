## Services
Services offer loadbalancing, service discovery and networking , End user can also access it.

### LoadBalancing
> Do minikube ssh
> Run the following command to make 20 curl requests
> for i in {1..20}; do curl http://<IP>:<PORT>; done
> run following commands to watch logs of all the pods
> kubectl logs nameOfThePod -f
> You will see the result that load gets distributed


### Port
Is the port on which the service object will be recieving the traffic

### TartgetPort
On which the container is running on the pod

### endpoints
Whenever a service is created an endpoint object is created with the same name as service, Pods which are associated with service thier IP is called endpoints.
```bash
kubectl get endpoints
#or
kubectl describe service/serviceName
```
## Types of services

### ClusterIP
This service exposes the pod on the IP which is accessible inside the cluster.We can access it outside the cluster also by port forwarding.But when we do port-forwarding we never get loadbalancing, It selects a pod and always sent traffic to it.
