1. From the Jump Host server, Secure copy the banner to the /tmp directory of the App Server. NOTE: this will be done for all 3 app servers(stapp01,stapp02,stapp03)
```
scp -r /home/thor/nautilus_banner tony@stapp01:/tmp
scp -r /home/thor/nautilus_banner steve@stapp02:/tmp
scp -r /home/thor/nautilus_banner banner@stapp03:/tmp
```

2. SSH into each server and move the nautilus banner from the /tmp to the /etc/motd directory
```
mv /tmp/nautilus_banner /etc/motd
```

3. For the database server, SSH into the server and install openssh-clients
```
ssh peter@stdb01
sudo -i
yum install -y openssh-clients
```

4. From the jump server, REPEAT STEP1 and STEP2 to transfer the banner to the server

5. To check the effect of the banner added to the servers, Log out of the server and log in. Banner will be displayed on entry