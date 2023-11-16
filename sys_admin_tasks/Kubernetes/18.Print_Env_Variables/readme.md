## Task:

The Nautilus DevOps team is working on to setup some pre-requisites for an application that will send the greetings to different users. There is a sample deployment, that needs to be tested. Below is a scenario which needs to be configured on Kubernetes cluster. Please find below more details about it.

1. Create a pod named `print-envars-greeting`.

2. Configure spec as, the container name should be `print-env-container` and use `bash` image.

3. Create three environment variables:

* `GREETING` and its value should be `Welcome to`

* `COMPANY` and its value should be `DevOps`

* `GROUP` and its value should be `Industries`

4. Use command to `echo ["$(GREETING) $(COMPANY) $(GROUP)"]` message.

5. You can check the output using `kubectl logs -f print-envars-greeting` command.