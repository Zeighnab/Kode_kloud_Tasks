1. SSH into all App Servers

2. Create a group
```
groupadd nautilus_noc
```

3. Create the given user and add to the group
```
useradd -G nautilus_noc mohammed
```

4. Verify
```
id mohammed
```