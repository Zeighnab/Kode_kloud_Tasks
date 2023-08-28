1. SSH into the storage server

2. cd into the beta directory
```
cd /usr/src/kodekloudrepos/beta
```

3. Confirm if the branch `xfusioncorp_beta`exist, then checkout to another branch
```
git branch
git checkout master
```

4. Delete the given branch
```
git branch -D xfusioncorp_beta
```