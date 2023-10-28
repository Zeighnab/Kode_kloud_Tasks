1. Create a replicaset using declarative method
```
vi replicaset.yaml

kubectl apply -f replicaset.yaml
```

2. Check the newly created replicaset
```
kubectl get replicaset

OR

k get rs
```

![](./img/1.png)

3. Validate the replica pods are running
```
kubectl get pod
```

![](./img/2.png)