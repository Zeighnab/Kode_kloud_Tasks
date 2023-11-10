1. Verify deployment and service
```
kubectl get deploy

kubectl get svc
```

![](./img/1.png)

2. Edit service to change `nodeport`
```
kubectl edit service nginx-service
```

![](./img/2.png)

3. Edit deployment to change `replicas` and `image`
```
kubectl edit deployment nginx-deployment
```

![](./img/3.png)

4. Validate successful changes
```
kubectl get all
```

![](./img/4.png)