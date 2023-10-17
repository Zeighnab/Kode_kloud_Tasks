1. Check for existing deployment in the cluster
```
kubectl get all
```

2. Create and Execute a yaml file named `nginx-deploy.yaml`.
```
vi nginx-deploy.yaml

kubectl apply -f pod-nginx.yaml
```

3. Validate a runnung deployment
```
kubectl get deploy
```