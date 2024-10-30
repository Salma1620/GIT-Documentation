# GIT-Documentation

# Table of content
- [What is GIT](#What-is-GIT)
- [GIT configuration commands](#GIT-configuration-commands)
- [GIT workspace commands](#GIT-workspace-commands)
- [GIT branches commands](#GIT-branches-commands)
- [GIT stage commands](#GIT-stage-commands)
- [GIT stash Commands](#GIT-stash-Commands)
- [Local repository commands](#Local-repository-commands)


# What is GIT
> - Git is a version control system VCG widely used for tracking changes in code during software development.<br/>
> - It enables developers to collaborate, keep version histories, and manage multiple branches in a project.<br/>

# GIT configuration commands
```
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```
This configures your identity for all Git repositories on your system.

# GIT workspace commands
To initialize a new Git repository:
```
git init
```
To clone an existing repository:
```
git clone <repository-url>
```
To check the status of the repo:
```
git status
```

# GIT branches commands
To create a new branch:
```
git branch <branch-name>
```
To switch to a branch:
```
git checkout <branch-name>
```
To create and switch to a new branch in one command:
```
git checkout -b <branch-name>
```
Merging other branch in actual branch
```
git merge <branchname>
```
Delete branch :
```
git branch -d <branchname>
```

## Viewing Differences
Show changes between your workspace and the staging area (unstaged changes)
```
git diff
```
Show changes between the staging area and the last commit (staged changes):
```
git diff --cached
```
removing a file from the workspace
```
git rm <file-name>
```

# GIT stage commands
Add files from the workspace to the staging area (index) to prepare them for a commit:
```
git add <file-name>
```
Add all modified files to staging:
```
git add .
```
## Removing Files from Staging
Unstage a specific file (remove it from the staging area but keep the changes in your workspace):
```
git reset <file-name>
```
Unstage all files:
```
git reset
```
# GIT stash Commands
> - git stash is a helpful Git command that temporarily saves your changes in the workspace without committing them, allowing you to switch branches or perform other tasks without losing your uncommitted work.<br/>
> - You can then reapply (or "unstash") those changes when you're ready to continue working on them.<br/>

Stash all tracked (added to Git) changes in the workspace:
```
git stash
```
Stash all changes, including untracked and ignored files:
```
git stash -u
```
You can also give a name (message) to your stash:
```
git stash save "stash message"
```
View Stash List:
```
git stash list
```
Reapply the most recent stash:
```
git stash apply
```
Apply a specific stash from the list:
```
git stash apply stash@{1}
```
Remove a specific stash without applying it:
```
git stash drop stash@{1}
```
Commit changes with message:
```
git commit -m "message"
```
Clear all stashes:
```
git stash clear
```
# Local repository commands
View the history of commits in your local repository:
```
git log
```
#  Reset Commits
Undo the last commit but keep changes in the workspace:
```
git reset --soft HEAD~1
```
Undo the last commit and remove changes from the workspace:
```
git reset --hard HEAD~1
```
Discard changes in a specific file by restoring it to its last committed state:
```
git checkout -- <file-name>
```
Checking Out a Specific Commit
```
git checkout <commit-hash>
```

# Remote reposiroty related commands
Fetching Changes from Remote
```
git fetch origin
```
> Fetch changes from the remote repository without merging them into your local branch. This updates your local copy of the remote branches <br/>

## Pulling Changes from Remote
Pull and merge changes from a remote branch into your current branch:
```
git pull origin <branch-name>
```

##  Pushing Changes to Remote
Push your committed changes to a remote branch:
```
git push origin <branch-name>
```
To push a new branch to the remote repository:
```
git push -u origin <branch-name>
```
View all remote branches:
```
git branch -r
```
Show both local and remote branches:
```
git branch -a
```
Deleting a Remote Branch:
```
git push origin --delete <branch-name>
```


















