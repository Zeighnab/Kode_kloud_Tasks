1. Login to App Server 3

2. Check the running container.
    docker ps -a

3. Open a shell to the container using `exec` command
    docker exec -it kkloud /bin/bash


4. Inside the container, install the necessary packages and configure the required settings based on the instructions.
    apt install apache2 -y
    cd  /etc/apache2
    sed -i 's/Listen 80/Listen 3003/g' ports.conf
    sed -i 's/:80/:3003/g' apache2.conf
    sed -i 's/#ServerName www.example.com/ServerName localhost/g' apache2.conf

*Note: SED command is used in searching, find and replace, insertion or deletion.* 

5. Restart the service and verify status.
    service apache2 start
    service apache2 enable
    service apache2 status  