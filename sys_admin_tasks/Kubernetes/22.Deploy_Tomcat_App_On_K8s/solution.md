1. Create the given namespace
```
kubectl create namespace tomcat-namespace-devops

kubectl get namespace
```

![](./img/1.png)

2. Create the deployment and service as per task
```
vi tomcat.yaml

kubectl create -f tomcat.yaml
```

![](./img/2.png)

3. Verify a running application

![](./img/3.png)