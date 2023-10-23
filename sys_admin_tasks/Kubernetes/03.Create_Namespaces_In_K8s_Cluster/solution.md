1. Validate namespaces present in the cluster
```
kubectl get namespaces

OR

kubectl get pods --all-namespaces
```

2. Create a namespace named `dev`
```
kubectl create namespace dev
```

3. Create a pod under the namesapce
```
kubectl create -f dev-pod.yaml
```

4. Validate the running pod in the namespace
```
kubectl get pod -n dev
```