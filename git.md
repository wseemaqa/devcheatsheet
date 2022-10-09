# GIT   

## INSTALLATION

**GitHub for Windows**
[htps://windows.github.com](htps://windows.github.com)

**GitHub for Mac**
[htps://mac.github.com](htps://mac.github.com)

*For Linux and Solaris platforms, the latest release is available on
the official Git web site.*
**Git for All Platforms**
[http://git-scm.com](http://git-scm.com)

## SETUP
__To configure user information used across all local repositories.__

*set a name that is identifiable for credit when review version history*
```
git config --global user.name “[firstname lastname]”
```
*set an email address that will be associated with each history marker*
```
git config --global user.email “[valid-email]”
```
*set automatic command line coloring for Git for easy reviewing*
```
git config --global color.ui auto
```

## SETUP AND INIT
__Configuring user information, initializing and cloning repositories__

**initialize an existing directory as a Git repository**
```
git init
```
**retrieve an entire repository from a hosted location via URL**
```
git clone [url]
```

## STAGING
**show modified files in working directory, staged for your next commit**
```
git status
```

**add a file as it looks now to your next commit (stage)**
```
git add <filenames>
```
**Tip: git add . adds all files in the current directory.**

**diff of what is changed but not staged**
```
git diff
```

_diff of what is staged but not yet commited_
```
git diff --staged
```

 _Display record of commits made_
```
git log
```

# BRANCHING AND MERGING
__List your branches. a * will appear next to the currently active branch__
```
git branch
```

__Create a new branch.__
```
git branch <branch name>
```

__Create branch and changes to it.__
```
git switch -c <branch name>
or
git checkout -b <branch name>
```

__Change to specified branch.__
```
git switch <branch name>
or
git checkout <branch name>
```

__Change to last branch used.__
```
git switch -
```

# REMOTE, PUSH & PULL
__Show tracked repos.__
```
git remote -v	
```

__Push changes to the default remote repo.__
```
git push
```	
*Tip: you can specify the name of another tracked repo after "push".*

__Pull changes from default remote repo and merges them into local.__
```
git pull
```

__Pull changes from default remote repo but do not merg into local.__
```
git fetch
```

__Roll back and reset the last staged commit.__
```
git reset HEAD~1
```
*Tip: The number specifies how much commits to reset by, git reset HEAD~2 rolls back 2 commits etc.*


__Squash multiple commits into one commit.__

_squash last 4 commits:_
```
git rebase -i HEAD~4
```
*Note: This command will open up default editor then replace "pick" on the second and subsequent commits with "squash".*
	
__Squash all commits:__
```
git rebase --root -i
```
*Note: This command will open up default editor then replace "pick" on the second and subsequent commits with "squash".*

__Stash the current state of the working directory__
```
git stash
```

__Remove the stashed code and apply it in the current working directory__
```
git stash pop
```

__Remove all stashed entries__
```
git stash clear
```

__Remove new/existing files from staged files__
```
git restore --staged <file_name>
```

_Cherry Pick enables arbitrary Git commits to be picked by reference and appended to the current working HEAD._  
			
__cherry pick a commit on to main branch:__
```
git cherry-pick commitSHA
```

__Command to merge a specific branch into the current branch__
```
git merge <branch name>
```
__To resolve merge conflict manually open the merge tool__
```
git mergetool
```
__To remove untracked files from the working directory__
```
git clean 
```
