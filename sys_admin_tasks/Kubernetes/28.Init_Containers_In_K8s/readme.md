## Task:

There are some applications that need to be deployed on Kubernetes cluster and these apps have some pre-requisites where some configurations need to be changed before deploying the app container. Some of these changes cannot be made inside the images so the DevOps team has come up with a solution to use init containers to perform these tasks during deployment. Below is a sample scenario that the team is going to test first.

1. Create a Deployment named as `ic-deploy-devops`.

2. Configure spec as replicas should be `1`, labels `app` should be `ic-devops`, template's metadata lables app should be the same `ic-devops`.

3. The initContainers should be named as `ic-msg-devops`, use image `fedora`, preferably with latest tag and use command:

    * '/bin/bash', 

    * '-c' and,

    * 'echo Init Done - Welcome to xFusionCorp Industries > /ic/official'. 

__The volume mount should be named as `ic-volume-devops` and mount path should be `/ic`.__

4. Main container should be named as `ic-main-devops`, use image `fedora`, preferably with latest tag and use command: 

    * '/bin/bash', 

    * '-c' and, 

    * 'while true; do cat /ic/official; sleep 5; done'. 

__The volume mount should be named as `ic-volume-devops` and mount path should be `/ic`.__


5. Volume to be named as `ic-volume-devops` and it should be an `emptyDir` type.