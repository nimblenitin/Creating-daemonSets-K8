# Creating-daemonSets-K8
A DaemonSet ensures that all (or some) Nodes run a copy of a Pod. It can be used to run a log Pod on each node. Nodes which have a taint may opt out in creation of Pods with daemonSets.

Simple example to run a Pod with daemonSet-

Steps followed:

*As Root*
```

1. Create the daemonSets YAML file.
$ kubectl vi daemonSets.yaml  
  
2. Create the Pod.
$ kubectl apply -f daemonSets.yaml --record

3. Check whether the Pod was created in the all the nodes
$ kubectl get pods -o wide

```
*As Root*
