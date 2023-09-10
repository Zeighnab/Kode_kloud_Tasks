1. SSH into Storage Server

2. Create a new branch from `master` in the `/usr/src/kodekloudrepos/news` directory
```
cd /usr/src/kodekloudrepos/news

git branch

git branch xfusion
```

3. Checkout to xfusion branch, then copy `index.html` file
```
git checkout xfusion

sudo cp /tmp/index.html .
```

4. Add/Commit the file
```
git add .

git commit -m 'index.html'
```

5. Merge the new branch to master branch
```
git checkout master

git merge xfusion
```

6. Push changes to remote repo
```
git push -u origin master
```