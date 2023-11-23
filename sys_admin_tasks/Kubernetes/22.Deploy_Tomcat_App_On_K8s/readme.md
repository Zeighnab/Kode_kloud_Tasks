## Task:

A new java-based application is ready to be deployed on a Kubernetes cluster. The development team had a meeting with the DevOps team to share the requirements and application scope. The team is ready to setup an application stack for it under their existing cluster. Below you can find the details for this:

1. Create a namespace named `tomcat-namespace-devops`.

2. Create a deployment for tomcat app which should be named as `tomcat-deployment-devops` under the same namespace you created. 

3. Replica count should be `1`, the container should be named as `tomcat-container-devops`, its image should be `gcr.io/kodekloud/centos-ssh-enabled:tomcat` and its container port should be `8080`.

4. Create a service for tomcat app which should be named as `tomcat-service-devops` under the same namespace you created. Service type should be `NodePort` and nodePort should be `32227`.

5. Click on `App` button to make sure the application is up and running.

6. You can use any labels as per your choice.