1. SSh into app-server 1

    ssh tony@stapp01

2. Login as root user

    sudo -i

3. create a new user 'yousuf' with no interactive shell

    useradd yousuf -s /sbin/nologin

4. Verify user creation

    cat /etc/passwd