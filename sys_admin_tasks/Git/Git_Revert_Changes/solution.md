1. SSh into Storage Server

2. Navivagte to the given repo, check git status
```
cd /usr/src/kodekloudrepos/games

git status
```

3. Check git logs
```
git log
```

4. Revert the last commit `HEAD`, then add/commit the new changes
```
git revert HEAD

git add .

git commit -m 'revert games'
```

Validate the task by checking the git log