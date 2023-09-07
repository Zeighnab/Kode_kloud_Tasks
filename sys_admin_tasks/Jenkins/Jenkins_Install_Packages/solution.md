1. Access Jenkins UI to login

2. Install the necessary plugins

![](./img/1.png)

3. Add credentials of the storage server

![](./img/2.png)

![](./img/3.png)

![](./img/4.png)

4. Under `Manage Jenkins` --> `Configure System` --> `SSH sites`, to allow connection from the server to jenkins. 

* Note: Check for successful connection

![](./img/5.png)

![](./img/6.png)

![](./img/7.png)

5. Create a job `install-packages`

![](./img/8.png)

6. Add a string parameter named `PACKAGE`

![](./img/9.png)

7. Under `install-packages` job --> `Configuration` --> `Build Steps` --> `Execute shell script on remote host using ssh`, give the necessary command

```
echo <storage-server-password> | sudo -S yum install -y $PACKAGE
```

![](./img/10.png)

8. To verify connection between the server and jenkins, install a package {nginx}, using `Build with parameters`

![](./img/11.png)

![](./img/12.png)

![](./img/13.png)