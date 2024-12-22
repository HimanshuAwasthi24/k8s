## Definition
A pod is sandboxed environment which is containing the container, Think of a machine which having an application inside it. It is the smallest unit in kubernetes.
It can have one or more containers.

## sidecar containers
A sidecar container is a helper or supporting container which running inside the pod with application container.
The sidecar container extends or enhances the functionality of the main application container by sharing 
the same networking namespace, storage volumes, and lifecycle.

## Creating pods

### Imperative way
```bash
# If we don't specify tag in image it will pick latest one
kubectl run PodName --image=nginx

#list the created pod
kubectl get pods
```
### Declarative way
We can achieve this by creating pod manifest file using yaml.</br>
**note:** `refer pods.yaml from repo`

### Get api resources
```bash
kubectl api-resources | grep ResourceName
```
### Enter inside the pod
```bash
kubectl exec -it podName -- bash
```
### Port forward
```bash
kubectl port-forward podName local-port:container-port
```

### Logs, Describe & delete
```bash
# Logs
kubectl logs podName

#describe 
kubectl describe pod podName

#delete resources refering yaml
kubectl delete -f pods.yaml

# delete individual resource
kubectl delete po/podName

```