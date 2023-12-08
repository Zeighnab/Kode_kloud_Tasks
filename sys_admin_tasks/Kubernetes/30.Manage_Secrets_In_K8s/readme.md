## Task:

The Nautilus DevOps team is working to deploy some tools in Kubernetes cluster. Some of the tools are licence based so that licence information needs to be stored securely within Kubernetes cluster. Therefore, the team wants to utilize Kubernetes secrets to store those secrets. Below you can find more details about the requirements:

* We already have a secret key file `ecommerce.txt` under `/opt` location on jump host. 

* Create a generic secret named `ecommerce`, it should contain the password/license-number present in `ecommerce.txt` file.

* Also create a pod named `secret-xfusion`.

* Configure pod's spec as container name should be `secret-container-xfusion`, image should be `centos` preferably with latest tag. Use sleep command for container so that it remains in running state. 

* Consume the created secret and mount it under `/opt/cluster` within the container.

* To verify you can exec into the container `secret-container-xfusion`, to check the secret key under the mounted path `/opt/cluster`.