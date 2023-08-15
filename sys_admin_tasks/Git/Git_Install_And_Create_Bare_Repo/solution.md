1. SSh into Storage Server
```
ssh natasha@ststor01
sudo su -
```

2. Install git
```
yum install git -y
```

3. Create (Initialize) a `bare` repository
```
git init --bare /opt/official.git
```