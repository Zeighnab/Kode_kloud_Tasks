1. Create a namespace called `devops`
```
kubectl create namespace devops

kubectl get namespace
```

![](./img/1.png)

2. Create the deployment file with all the parameters, and allow the pods to be in a running state
```
kubectl apply -f devops.yaml

kubectl get pods -n devops
```

![](./img/2.png)

3. Perform a rolling update
```
kubectl set image deployment httpd-deploy  httpd=httpd:2.4.43 --namespace devops

kubectl describe pod {pod-name} -n devops
```

![](./img/3.png)

![](./img/4.png)

4. Rollback the deployment as per task
```
kubectl rollout undo deployment httpd-deploy  -n devops

kubectl describe pod {pod-name} -n devops
```

![](./img/5.png)