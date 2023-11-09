1. Check the pod for errors
```
kubectl describe pod webserver
```

![](./img/1.png)

2. Edit the pod file to correct the error
```
kubectl edit pod webserver
```

![](./img/2.png)

3. Validate running pod
```
kubectl get pod
```

![](./img/3.png)