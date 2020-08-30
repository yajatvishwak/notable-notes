---
title: Git Commands I always forget
created: '2020-08-29T07:23:19.138Z'
modified: '2020-08-30T13:08:21.522Z'
---

# Git Commands I always forget

Open Terminal.
Change the current working directory to your local project.
# 1. Initialize the local directory as a Git repository.
```bash
$ git init
```
# 2. Add the files in your new local repository. This stages them for the first commit.
```bash
$ git add .
```
#### Adds the files in the local repository and stages them for commit. To unstage a file, use 'git reset HEAD YOUR-FILE'.
# 3. Commit the files that you've staged in your local repository.
```bash 
$ git commit -m "First commit"
```
#### Commits the tracked changes and prepares them to be pushed to a remote repository. To remove this commit and modify the file, use 'git reset --soft HEAD~1' and commit and add the file again.
At the top of your GitHub repository's Quick Setup page, click  to copy the remote repository URL.
Copy remote repository URL field


# 4. Add branch
```bash 
git branch -M master
```
# 5. Set the new remote
```bash 
$ git remote add origin <remote repository URL>
```
# 6. Push the changes in your local repository to GitHub.
```bash
git push -u origin master
```

# After git initialization
- git push
- git pull

