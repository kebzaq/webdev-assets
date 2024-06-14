# GIT Cheatsheet

### Useful GIT commands

- git clone [remote-repo-link]
  - to make a local copy of remote repo
- git init
  - to make project/folder git folder – only one time
- git add . (or file name instead dot)
  - add all changed files / or listed file to git
- git commit –m "your message here"
  - commit your changes
- git add . ; git commit -m “your message here”
  - 2 commands in one line
- git push
  - push changes to git
- git push -u origin [main-or-feature-branch-name]
  - first time only
- git push --set-upstream origin [main-or-branch]
  - first time only
    -Note: create pull request on github and merge code to main after approval
- git pull
  - update your local from remote - pull only when on main branch

### Create new branch:

- git branch [new-branch-name]
  - create new branch
- git checkout -b [new-branch-name]
  - create branch and switch
- git branch -m [new-branch-name]
  - rename branch
  - Note: Types of branches:
    - Feature branch
    - For fixing a bug

### Delete branch on local

- git branch -d [branch-name]
  - to delete merged branch
- git branch –D [branch-name]
  - to delete un-merged branch
- git push origin --delete [new-branch-name]
  - to delete new branch on remote

### Stash commands:

- git stash
  - to stash your changes before git pull
- git stash pop
  - to return back your stashed changes
- git stash drop
  - to delete your stashed changes

### Other git commands:

- git status
  - to check which files are added to commit
- git log
  - to check your commits
- git log -oneline
  - to check your commits and id in one line
- git remote –v
  - to check remote connection status

### How to remove commit but save the changes

- git reset --soft HEAD^

### How to remove commit and all changes

- git reset --hard HEAD^

### How to un-git your project

- ls –a
  - to see hidden .git folder
- rm –rf .git.
  - to remove .git folder

### How to REBASE

1. git pull
   - to pull latest on main branch
2. git checkout [branch-name]
   - to switch to feature branch
   - git stash (if you have changes/updates on feature branch)
3. git rebase origin/main
   - update feature branch from main
   - git stash pop (to get stashed changes back)

### How to MERGE

1. git merge

   - Merge from main to feature branch:
     - git merge [feature-branch] (on main branch and change first line message on VIM)
   - Merge from feature to main:
     - git merge main (on feature branch)

2. git merge –squash

### Git config commands:

- git config --global –edit
  - to edit
- git config --global –list
  - to see all global list
- git config --global push.default current
- git config --global push.autoSetupRemote true

### Adding alias:

- git config --global alias.co checkout
- git config --global alias.br branch
- git config --global alias.ci commit
- git config --global alias.st status
