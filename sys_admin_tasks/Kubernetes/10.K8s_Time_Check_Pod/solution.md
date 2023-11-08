1. Create the `nautilus` namespace
```
kubectl create namespace nautilus
```

2. Create a configmap `(time-config)` and pod `(time-check)` in the nautilus namespace
```
vi time-check.yml

kubectl apply -f time-check.yml
```

3. Log into the container to validate the logs
```
kubectl exec -n nautilus -it time-check -- /bin/sh

cat /opt/security/time/time-check.log
```