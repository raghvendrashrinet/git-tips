### create a new repository on the command line
```
echo "# git-tips" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/raghvendrashrinet/git-tips.git
git push -u origin main
```
### push an existing repository from the command line
```
git remote add origin https://github.com/raghvendrashrinet/git-tips.git
git branch -M main
git push -u origin main
```
### When Your local branch is named master, but the remote repository uses main
#### Option 1: Rename Local Branch to Match Remote
This is the cleanest approach if you want to follow the remote’s naming convention (main)
```
# Rename local branch from master to main
git branch -m master main

# Update the upstream tracking to point to remote main
git push -u origin main
```
#### Option 2: Keep Local master and Link It to Remote main
If you prefer not to rename your local branch:
```
# Tell Git that local master should track remote main
git branch --set-upstream-to=origin/main master

# Push changes from local master to remote main
git push origin master:main

```
### To get the remote files into your local repo, you need to fetch or pull:
```
git fetch origin
git pull origin main
```
# (Optional) delete the old master branch from remote if it exists
git push origin --delete master
```
