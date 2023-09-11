1. SSH into Storage Server

2. Navigate to the cloned directory
```
cd usr/src/kodekloudrepos/games
```

3. Add remote and point to the given repo
```
git remote dev_games /opt/xfusioncorp_games.git
```

4. Copy the HTML file
```
sudo cp index.html .
```

5. Initialize the new repo, then add/commit the new file added
```
git init

git add .

git commit -m 'added index.html'
```

6. Push to master branch
```
git push -u dev_games master
```