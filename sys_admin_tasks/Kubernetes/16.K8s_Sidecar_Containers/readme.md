# Sidecar Containers:
A sidecar container is a design pattern that allows you to run an additional container alongside your main container in the same pod. The sidecar container can perform tasks that complement the main container, such as syncing data from a remote source, collecting and shipping logs, providing health checks and metrics, proxying network traffic, encrypting or decrypting data, or injecting faults for testing.

The sidecar container shares the same lifecycle, resources, and network namespace as the main container but has its own file system and process space. This means that the sidecar container can access the same ports, volumes, and environment variables as the main container but cannot interfere with its execution

## Scenerio:

We have a web server container running the nginx image. The access and error logs generated by the web server are not critical enough to be placed on a persistent volume. However, Nautilus developers need access to the last 24 hours of logs so that they can trace issues and bugs. Therefore, we need to ship the access and error logs for the web server to a log-aggregation service. Following the separation of concerns principle, we implement the Sidecar pattern by deploying a second container that ships the error and access logs from nginx. Nginx does one thing, and it does it well—serving web pages. The second container also specializes in its task—shipping logs. Since containers are running on the same Pod, we can use a shared emptyDir volume to read and write logs.

### Task:

1. Create a pod named `webserver`.

2. Create an `emptyDir` volume `shared-logs`.

3. Create two containers from `nginx` and `ubuntu` images with latest tag only and remember to mention tag i.e `nginx:latest`, nginx container name should be `nginx-container` and ubuntu container name should be `sidecar-container` on webserver pod.

4. Add command on sidecar-container `"sh","-c","while true; do cat /var/log/nginx/access.log /var/log/nginx/error.log; sleep 30; done"`

5. Mount the volume shared-logs on both containers at location `/var/log/nginx`, all containers should be up and running.