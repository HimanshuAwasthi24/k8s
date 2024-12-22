## ReplicaSets
Is resource in kubernetes which helps in running multiple instances of our pod, This capability provide self-healing and high-availability.

### Why do mention selector in ReplicaSet spec file?
Replicas picks up the pods which are not part of replica set while creating pods, Which were already created by the same labels.
**note: it can also pick up new nodes if the nodes on which the pods are running gets deleted**

## Rollout and rollbacks => Deployments
1. Rollouts:
