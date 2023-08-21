1. Copy index.html file from the jump host to storage server
```
sudo scp /tmp/index.html natasha@ststor01:/tmp
```

2. SSH into the storage server
```
ssh natasha@ststor01
sudo su -
```

3. Copy the givrn file to the cloned repository
```
cd usr/src/kodekloudrepos/cluster
ls
cp /tmp/index.html .
```

4. Add/Commit/Push the file to master branch
```
git add .
git commit -m "add index.html"
git push -u origin master
```