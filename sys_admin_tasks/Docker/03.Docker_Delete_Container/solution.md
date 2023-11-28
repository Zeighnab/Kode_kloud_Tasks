1. Login to App server 3 and switch to root
```
ssh banner@stapp03

sudo su -
```

2. Check the running container
    docker ps -a

3. Stop the container, the delete
    docker stop kke-container

    docker rm kke-container

    docker ps -a