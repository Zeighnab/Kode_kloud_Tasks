1. Check for existing pods in the cluster
```
kubectl get pods
```

2. Create and Execute a yaml file named `pod-nginx.yaml`.
```
vi pod-nginx.yaml

kubectl apply -f pod-nginx.yaml
```

3. Validate the running pod
```
kubectl get po
```