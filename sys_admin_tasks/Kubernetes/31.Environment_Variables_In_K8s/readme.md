## Task:

There are a number of parameters that are used by the applications. We need to define these as environment variables, so that we can use them as needed within different configs. Below is a scenario which needs to be configured on Kubernetes cluster. Please find below more details about the same.

1. Create a pod named `envars`.

2. Container name should be `fieldref-container`, use image `httpd` preferable latest tag, use command `'sh', '-c'` and args should be

```
'while true; do echo -en '/n'; printenv NODE_NAME POD_NAME; printenv POD_IP POD_SERVICE_ACCOUNT; sleep 10; done;'
```

* Please take care of indentations

3. Define Four environment variables as mentioned below:

* The first env should be named as `NODE_NAME`, set valueFrom fieldref and fieldPath should be `spec.nodeName`.

* The second env should be named as `POD_NAME`, set valueFrom fieldref and fieldPath should be `metadata.name`.

* The third env should be named as `POD_IP`, set valueFrom fieldref and fieldPath should be `status.podIP`.

* The fourth env should be named as `POD_SERVICE_ACCOUNT`, set valueFrom fieldref and fieldPath shoulbe be `spec.serviceAccountName`.

4. Set restart policy to `Never`.

5. To check the output, exec into the pod and use `printenv` command.

