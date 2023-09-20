1. SSH into Storage Server

2. Navigate to the given repo
```
cd /usr/src/kodekloudrepos/news
```

3. Check the logs
```
git log
```

4. Reset the git commit history
```
git reset --hard HEAD~10
```

* Note: `git reset --hard` is used to reset the current branch to a previous commit, discarding any local changes and modifications made to the files. This command will reset the current branch to the commit that is 10 steps back from the current HEAD pointer.

6. Push changes to remote repo
```
git push --force
```