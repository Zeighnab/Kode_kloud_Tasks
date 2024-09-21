1. SSH into App server 3
```
ssh banner@stapp03
```

2. Create a user with the given UID and home directory
```
useradd -u 1691 -d /var/www/kirsty kirsty
```

3. Verify
```
cat /etc/passwd
```