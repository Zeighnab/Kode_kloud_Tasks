1. SSH into Storage Server

2. Navigate into the given directory
```
cd /usr/src/kodekloudrepos/beta
```

3. Check the logs of the feature branch
```
git log
```

4. Checkout to master branch
```
git checkout master
```

5. Pick the commit `Update info.txt` from the feature branch to the master branch
```
git cherry-pick {commit-ref}
```

6. Push changes to remote repo
```
git push origin -u master
```