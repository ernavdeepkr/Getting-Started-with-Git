# 1. GIT
<a id="markdown-GIT" name="GIT"></a>

> PDF File available in the repo but best view available in README.md file.
<!-- TOC -->

- [1. GIT](#1-git)
  - [1.1. Introduction](#11-introduction)
  - [1.2. Version Control System](#12-version-control-system)
    - [1.2.1. Centralizted version conrol system (CVCS)](#121-centralizted-version-conrol-system-cvcs)
    - [1.2.2. Distributed version control system (DVCS)](#122-distributed-version-control-system-dvcs)
  - [1.3. Github Vs Git](#13-github-vs-git)
  - [1.4. Install](#14-install)
  - [1.5. Git States](#15-git-states)
  - [1.6. Git Commands](#16-git-commands)
    - [1.6.1. Configuring git](#161-configuring-git)
      - [1.6.1.1. git config](#1611-git-config)
      - [1.6.1.2. color highlighting](#1612-color-highlighting)
      - [1.6.1.3. Setting default editor](#1613-setting-default-editor)
    - [1.6.2. Create repositories](#162-create-repositories)
    - [1.6.3. git clone](#163-git-clone)
    - [1.6.4. Make changes](#164-make-changes)
      - [1.6.4.1. git add](#1641-git-add)
      - [1.6.4.2. git commit](#1642-git-commit)
      - [1.6.4.3. git tag](#1643-git-tag)
      - [1.6.4.4. git log](#1644-git-log)
      - [1.6.4.5. git show](#1645-git-show)
      - [1.6.4.6. git diff](#1646-git-diff)
    - [1.6.5. Redo commits](#165-redo-commits)
    - [1.6.6. Check status](#166-check-status)
    - [1.6.7. Git Branches](#167-git-branches)
    - [1.6.8. Add Remote](#168-add-remote)
    - [1.6.9. Synchronise changes](#169-synchronise-changes)
      - [1.6.9.1. git push](#1691-git-push)
      - [1.6.9.2. git pull](#1692-git-pull)
      - [1.6.9.3. git fetch](#1693-git-fetch)
      - [1.6.9.4. git merge](#1694-git-merge)
      - [1.6.9.5. git rebase](#1695-git-rebase)
    - [1.6.10. Git stash](#1610-git-stash)
  - [1.7. Git ignore](#17-git-ignore)
  - [1.8. Git Fork](#18-git-fork)
  - [1.9. Git Alias](#19-git-alias)
  - [1.10. Git Hooks](#110-git-hooks)
- [2. **Frequently Asked Questions**](#2-frequently-asked-questions)
  - [2.1. What is a repository in Git?](#21-what-is-a-repository-in-git)
  - [2.2. Difference between clone and fork](#22-difference-between-clone-and-fork)
  - [2.3. Difference between rebase and merge](#23-difference-between-rebase-and-merge)
  - [2.4. Difference between pull and fetch](#24-difference-between-pull-and-fetch)
  - [2.5. What is a 'conflict' in git?](#25-what-is-a-conflict-in-git)
  - [2.6. How to resolve a conflict in Git?](#26-how-to-resolve-a-conflict-in-git)
  - [2.7. What is the difference between the 'git diff' and 'git status'?](#27-what-is-the-difference-between-the-git-diff-and-git-status)
  - [2.8. How will you know in Git if a branch has already been merged into master?](#28-how-will-you-know-in-git-if-a-branch-has-already-been-merged-into-master)
  - [2.9. Explain the difference between reverting and resetting.](#29-explain-the-difference-between-reverting-and-resetting)
  - [2.10. What is git cherry-pick?](#210-what-is-git-cherry-pick)

<!-- /TOC -->

## 1.1. Introduction
<a id="markdown-Introduction" name="Introduction"></a>
Git is an Open Source ***Distributed Version Control System*** designed to manage the teamwork done on a project. Git helps the contributors to track the changes in files or projects and speed up the overall process.
- **It is designed for :**
    - Speed
    - Simplicity
    - Fully Distributed
    - Excellent support for parallel development
    - Integrity
     
## 1.2. Version Control System 
<a id="markdown-Version%20Control%20System%20" name="Version%20Control%20System%20"></a>
  Version Control System (VCS) is a software that helps software developers to work together and maintain a complete history of their work.

- **Functions of a VCS :**
    - Allows developers to work simultaneously.
    - Does not allow overwriting each other’s changes.
    - Maintains a history of every version.
     
- **Types of VCS :** 

### 1.2.1. Centralizted version conrol system (CVCS)
<a id="markdown-Centralizted%20version%20conrol%20system%20(CVCS)" name="Centralizted%20version%20conrol%20system%20(CVCS)"></a>

*Centralized version control system (CVCS) uses a central server to store all files and enables team collaboration. But the major drawback of CVCS is its single point of failure, i.e., failure of the central server.*
![image courtsey abc.com](resources/img/CVCS.png)
        
### 1.2.2. Distributed version control system (DVCS)
<a id="markdown-Distributed%20version%20control%20system%20(DVCS)" name="Distributed%20version%20control%20system%20(DVCS)"></a>

*Distributed VCS introduced significant improvement over the risks posed by Central VCS.These systems do not necessarily rely on a central server to store all the versions of a project’s files. Instead, every developer "clones" a copy of a repository and has the full history of the project on their own hard drive. This copy (or "clone") has all of the metadata of the original.*
![Test Image 1](resources/img/DSCV.png)

## 1.3. Github Vs Git
<a id="markdown-Github%20Vs%20Git" name="Github%20Vs%20Git"></a>

  ![Test Image 1 ](resources/img/Git_github.png)  
  - **Github :** It is  web portal and cloud hosting service for your Git repositories.
  - **Git :** It is a Distributed Version Control System client for tracking versions of files.

 
## 1.4. Install
<a id="markdown-Install" name="Install"></a>
  - GitHub for Windows
  https://windows.github.com
  - GitHub for Mac
  https://mac.github.com
  - Git for All Platforms
  http://git-scm.com
  - Git distributions for Linux and POSIX systems are available on
  the official Git SCM web site.

## 1.5. Git States
<a id="markdown-Git%20States" name="Git%20States"></a>

  ![Test Image 1](resources/img/git_states.png)

  - **`Working area :`** 
Consider a project residing in your local system. This project may or may not be tracked by Git. In either case, this project directory is called your Working directory. Working directory is the directory containing .git folder.
In this state, Git is just aware of the files in the project. It doesn’t track the files yet. To track the files, we've to commit these files by first adding the files to the staging area.
    > **`Note :`** **git init** – Command to initialize a Git repository
  - **`Staging area :`** 
Staging area is the playground where you group, add and organize the files to be committed to Git for tracking their versions. Committing process is done in the staging area on the files which are added to the Index after git add command is executed. This committing process is done by the use of git commit command. This command commits the staged changes to the local repository
    > **`Note :`** **git add** – Command to add files to staging area.
  - **`Git repository :`**
Git repository is the database where metadata about project file's history will be tracked.Now that the files to be committed are grouped and ready in the staging area, we can commit these files. So, we commit this group of files along with a commit message explaining what is the commit about. Apart from commit message, this step also records the author and time of the commit. Now, a snapshot of the files in the commit is recorded by Git. The information related to this commit (names of files committed, date and time of commit, author of commit, commit message) is stored in the Git directory.
    > **`Note :`** **git commit -m "your message"** – Command to commit files to Git repository with message 
  - **`Remote repository :`**    
  It means mirror or clone of the local Git repository in Github. This will allow other collaborators to view the code. Thus, whatever changes you make in the local Git repository will be visible to other collaborators when you push your code to the remote repository. Command to push the code to remote repository in Github is git push.

    ![Test Image 1](resources/img/remote.png)
    > **`Note :`** 
    > - **git push** - Command to push commits from local Git repository to remote Git repository hosted in Github.
    > - **git pull** - Pull command is used to fetch the commits from a remote repository and stores them in the remote branches.


## 1.6. Git Commands
<a id="markdown-Git%20Commands" name="Git%20Commands"></a>

### 1.6.1. Configuring git 
<a id="markdown-Configuring%20git%20" name="Configuring%20git%20"></a>

*Configure user information for system level, user level and local repositories level*

#### 1.6.1.1. git config
<a id="markdown-git%20config" name="git%20config"></a>

*This command sets the author name and email address respectively to be used with your commits.*
```
: git config –-global user.name "FIRSTNAME LASTNAME"
: git config –-global user.email "abc@example.com"
: git config --global --list
```

#### 1.6.1.2. color highlighting
<a id="markdown-color%20highlighting" name="color%20highlighting"></a>

*The following commands enables color highlighting for Git in the console.*
```
git config --global color.ui auto
```

#### 1.6.1.3. Setting default editor
<a id="markdown-Setting%20default%20editor" name="Setting%20default%20editor"></a>

*By default, Git uses the system default editor, which is taken from the VISUAL or
EDITOR environment variable. We can configure a different one by using git
config.*
```
git config --global core.editor <editor>
# for example:
git config --global core.editor vim
git config --global core.editor emacs
```
> **`Note:`** 
> - One can use --global to set configs for global level 
> - --user for user level
> - without any option (git config core.editor vim) for project level.

### 1.6.2. Create repositories
<a id="markdown-Create%20repositories" name="Create%20repositories"></a>

*When starting out with a new repository, you only need to do it
once either locally and adding remote url, then push to GitHub, or by cloning an
existing repository.*
  - **git init :** This command is used to start a new repository.
    ```
    git init [repository name]
    git remote add origin https://github.com/example/project.git
    ```
   
### 1.6.3. git clone
<a id="markdown-git%20clone" name="git%20clone"></a>

*This command is used to obtain a repository from an existing URL.*
    ```
    git clone [url]
    ```

### 1.6.4. Make changes
<a id="markdown-Make%20changes" name="Make%20changes"></a>

*Browse and inspect the evolution of project files*

#### 1.6.4.1. git add 
<a id="markdown-git%20add%20" name="git%20add%20"></a>

*This command adds a file to the staging area.*
```
git add [file]  
```
- This command adds one or more to the staging area.
```
git add *  
```

#### 1.6.4.2. git commit 
<a id="markdown-git%20commit%20" name="git%20commit%20"></a>

*This command records or snapshots the file permanently in the version history.*
```
git commit -m "[Type the commit message]"
```
- This command commits any files you've added with the git add command and also commits any files you've changed since then.
```
git commit -a  
```

#### 1.6.4.3. git tag 
<a id="markdown-git%20tag%20" name="git%20tag%20"></a>
 
*This command is used to give tags to the specified commit.*
```
git tag [commitID]
```  

#### 1.6.4.4. git log
<a id="markdown-git%20log" name="git%20log"></a>

*This command is used to list the version history for the current branch.*
```
git log  
```
- **decorated log** [add alias: `git config --global alias.lga "log --graph --oneline --all --decorate"`]
```
git log --graph --oneline --all --decorate
git lga (if alias added)
```

#### 1.6.4.5. git show 
<a id="markdown-git%20show%20" name="git%20show%20"></a>

*This command shows the metadata and content changes of the specified commit.*
```
git show [commit]  
```

#### 1.6.4.6. git diff
<a id="markdown-git%20diff" name="git%20diff"></a>

*This command shows the file differences which are not yet staged.*
```
git diff  
```
- This command shows the differences between the files in the staging area and the latest version present.
```
git diff --staged 
```
- This command shows the differences between the two branches mentioned.
```
git diff [first branch] [second branch]  
```

### 1.6.5. Redo commits
<a id="markdown-Redo%20commits" name="Redo%20commits"></a>

*Erase mistakes and craft replacement history*
- **git reset :** This command unstages the file, but it preserves the file contents.
```
git reset [file]  
```
- This command undoes all the commits after the specified commit and preserves the changes locally.
```
git reset [commit]  
```
- This command discards all history and goes back to the specified commit.
```
git reset --hard [commit] 
```

### 1.6.6. Check status
<a id="markdown-Check%20status" name="Check%20status"></a>
- **git status :** This command lists all the files that have to be committed.
```
git status  
```
- **git rm :** This command deletes the file from your working directory and stages the deletion.
```
git rm [file]  
```

### 1.6.7. Git Branches
<a id="markdown-Git%20Branches" name="Git%20Branches"></a>

*Branching means diverging from the mainline and continue to work separately without messing with the mainline.* 
 
![Test Image 1](resources/img/branch1.png)
  - **git branch :** 
      - This command lists all the local branches in the current repository.
        ```
        git branch  
        ```
    - This command creates a new branch
      ```
      git branch [branch name]  
      ```
    - This command deletes the feature branch.
      ```
      git branch -d [branch name]  
      ```
    - **git checkout :**
    This command is used to switch from one branch to another.
      ```
      git checkout [branch name]  
      ```
    - This command creates a new branch and also switches to it.
      ```
      git checkout -b [branch name]  
      ```

### 1.6.8. Add Remote 
<a id="markdown-Add%20Remote%20" name="Add%20Remote%20"></a>

*A common repository on GitHub that all team member use to exchange their changes*
  - **git remote :** This command is used to connect your local repository to the remote server.
    ```
    git remote add [variable name] [Remote Server URL]  
    ```

### 1.6.9. Synchronise changes
<a id="markdown-Synchronise%20changes" name="Synchronise%20changes"></a>

*Synchronize your local repository with the remote repository on GitHub.com*

#### 1.6.9.1. git push
<a id="markdown-git%20push" name="git%20push"></a>
*This command sends the committed changes of master branch to your remote repository.*
```
git push [variable name] master  
```
- This command sends the branch commits to your remote repository.
``` 
git push [variable name] [branch]  
```
- This command pushes all branches to your remote repository.
```
git push --all [variable name]  
```
- This command deletes a branch on your remote repository.
```
git push [variable name] :[branch name]  
```   

#### 1.6.9.2. git pull
<a id="markdown-git%20pull" name="git%20pull"></a>
*This command fetches and merges changes on the remote server to your working directory.*
```
git pull [Repository Link]  
``` 

#### 1.6.9.3. git fetch
<a id="markdown-git%20fetch" name="git%20fetch"></a>
 
*The git fetch command downloads commits, files, and refs from a remote repository into your local repo. Fetching is what you do when you want to see what everybody else has been working on.*
- Fetch all of the branches from the repository. This also downloads all of the required commits and files from the other repository.
``` 
git fetch <remote>
```
- Same as the above command, but only fetch the specified branch.
```
git fetch <remote> <branch>
``` 
- A power move which fetches all registered remotes and their branches:
```
git fetch --all
```
- The --dry-run option will perform a demo run of the command. 
```
git fetch --dry-run
```

#### 1.6.9.4. git merge
<a id="markdown-git%20merge" name="git%20merge"></a>

*This command merges the specified branch’s history into the current branch.*
```
git merge [branch name]  
```

#### 1.6.9.5. git rebase
<a id="markdown-git%20rebase" name="git%20rebase"></a>

*Rebase is another way to integrate changes from one branch to another. Rebase compresses all the changes into a single "patch." Then it integrates the patch onto the target branch.Unlike merging, rebasing flattens the history because it transfers the completed work from one branch to another. In the process, unwanted history is eliminated.*
- **Create a feature branch based of master**
```
git checkout -b feature_branch master
```
- **Make changes whatever you want**
- **commit your changes :**
```
git commit -a -m "Adds new feature"
```
- **git rebase :** This automatically rebases the current branch onto base.
```
git rebase <base>
```
- **Git Rebase Interactive :** *Running git rebase with the -i flag begins an interactive rebasing session. Instead of blindly moving all of the commits to the new base, interactive rebasing gives you the opportunity to alter individual commits in the process.*
```
git rebase --interactive <base>
```
- **Some git rebase interactive options :**
```
  pick 2231360 some old commit
  pick ee2adc2 Adds new feature
  # Rebase 2cf755d..ee2adc2 onto 2cf755d (9 commands)
  #
  # Commands:
  # p, pick = use commit
  # r, reword = use commit, but edit the commit message
  # e, edit = use commit, but stop for amending
  # s, squash = use commit, but meld into previous commit
  # f, fixup = like "squash", but discard this commit's log message
  # x, exec = run command (the rest of the line) using shell
  # d, drop = remove commit
```

### 1.6.10. Git stash
<a id="markdown-Git%20stash" name="Git%20stash"></a>

*Use git stash when you want to record the current state of the working directory and the index, but want to go back to a clean working directory. The command saves your local modifications away and reverts the working directory to match the HEAD commit.*
  - **git stash :** This command temporarily stores all the modified tracked files.
    ```
    git stash save  
    ```
  - This command restores the most recently stashed files.
    ```
    git stash pop  
    ```
  - This command lists all stashed changesets. 
    ```
    git stash list  
    ```   
  - This command discards the most recently stashed changeset.
    ```
    git stash drop  
    ```

## 1.7. Git ignore
<a id="markdown-Git%20ignore" name="Git%20ignore"></a>

*The .gitignore file is a text file that tells Git which files or folders to ignore in a project.
To create a local .gitignore file, create a text file and name it .gitignore (remember to include the DOT "." at the beginning).* 
  - **Steps to create a .gitignore file :**
    - Open Git Bash.
    - Navigate to the location of your Git repository.
  - **Create a .gitignore file for your repository.**
    ``` 
    $ touch .gitignore
    ```

## 1.8. Git Fork
<a id="markdown-Git%20Fork" name="Git%20Fork"></a>
*When you fork a repository, you create a copy of the original repository (upstream repository) but the repository remains on your GitHub account.* A fork is a copy of a repository. Forking a repository allows to freely experiment with changes without affecting the original project.
  - **Steps in git fork :**
    - **`Fork a Repository:`** User creates a copy of the repository to their own GitHub account.
    - **`Code changes:`** This involves git cloning. Here the user makes the changes and push back to their own forked repository.
    - **`Send changes to Original Repository:`** This process is called as Pull Request in Git. At this step, the user sends the changes to the owner of the repository as a request. Now it is up to the owner to accept the changes or reject. Pull request is a request to the owner of the upstream repository to accept the user changes.

## 1.9. Git Alias
<a id="markdown-Git%20Alias" name="Git%20Alias"></a>
*Aliases are used to create shorter commands that map to longer commands. Aliases enable more efficient workflows by requiring fewer keystrokes to execute a command.* 
- There is no direct git alias command. Aliases are created through the use of the git config command and the Git configuration files. As with other configuration values, aliases can be created in a local or global scope.
- These aliases were created with the --global flag which means they will be stored in Git's global operating system level configuration file. On linux systems, the global config file is located in the User home directory at ~/.gitconfig.
- **`Methods to create Git Alias :`** Aliases can be created through two primary methods.
  - **Directly editing Git config files :** The global or local config files can be manually edited and saved to create aliases.
    - **Examples :**
  ```
  [alias]
  co = checkout
  cm = commit -m
  po = push origin
  ci = commit --interactive
  cam = commit --amend --message
  lga = log --graph --all  --decorate --oneline
  ```
  - **Using the git config to create aliases :** git config command is a convenient utility to quickly create aliases. 
    - **Examples :**
  ```
  git config --global alias.co checkout
  git config --global alias.cm commit -m
  git config --global alias.po push origin
  git config --global alias.ci commit --interactive
  git config --global alias.cam commit --amend --message
  git config --global alias.lga log --graph --all  --decorate --oneline
  ```
 
## 1.10. Git Hooks
<a id="markdown-Git%20Hooks" name="Git%20Hooks"></a>
*Git hooks are scripts that Git executes before or after events such as: commit, push, and receive. Git hooks are a built-in feature - no need to download anything. Git hooks are run locally.*
  - **Some example hook scripts include :**
    - **`pre-commit :`** Check the commit message for spelling errors.
    - **`pre-receive :`** Enforce project coding standards.
    - **`post-commit :`** Email/SMS team members of a new commit.
    - **`post-receive :`** Push the code to production.  
  
  - *Every Git repository has a .git/hooks folder with a script for each hook you can bind to. You're free to change or update these scripts as necessary, and Git will execute them when those events occur.*

# 2. **Frequently Asked Questions**
<a id="markdown-**Frequently%20Asked%20Questions**" name="**Frequently%20Asked%20Questions**"></a>

## 2.1. What is a repository in Git?
<a id="markdown-What%20is%20a%20repository%20in%20Git%3F" name="What%20is%20a%20repository%20in%20Git%3F"></a>
  - Repository in Git is a place where Git stores all the files. Git can store the files either on the local repository or on the remote repository.
   
## 2.2. Difference between clone and fork
<a id="markdown-Difference%20between%20clone%20and%20fork" name="Difference%20between%20clone%20and%20fork"></a>
  - Forking is a concept while cloning is a process. Forking is just containing a separate copy of the repository and there is no command involved. Cloning is done through the command 'git clone' and it is a process of receiving all the code files to the local machine.

    ![Test Image 1](resources/img/fork.png)  
  
## 2.3. Difference between rebase and merge
<a id="markdown-Difference%20between%20rebase%20and%20merge" name="Difference%20between%20rebase%20and%20merge"></a>
  - Rebasing and merging are both designed to integrate changes from one branch into another branch but in different ways.The **merge** will result as a combination of commits, whereas **rebase** will add all the changes in feature branch starting from the last commit of the master branch:
  
    ![Test Image 1](resources/img/rebase.png) 

## 2.4. Difference between pull and fetch
<a id="markdown-Difference%20between%20pull%20and%20fetch" name="Difference%20between%20pull%20and%20fetch"></a>
  - In the simplest terms, git pull does a git fetch followed by a git merge. 
    > `Note :` Git pull = git fetch + git merge 

    ![Test Image 1](resources/img/pull_fetch_merge.png) 

## 2.5. What is a 'conflict' in git?
<a id="markdown-What%20is%20a%20'conflict'%20in%20git%3F" name="What%20is%20a%20'conflict'%20in%20git%3F"></a>
  - Git can handle on its own most merges by using its automatic merging features. There arises a conflict when two separate branches have made edits to the same line in a file, or when a file has been deleted in one branch but edited in the other. Conflicts are most likely to happen when working in a team environment.
   
## 2.6. How to resolve a conflict in Git?
<a id="markdown-How%20to%20resolve%20a%20conflict%20in%20Git%3F" name="How%20to%20resolve%20a%20conflict%20in%20Git%3F"></a>
  - **The following steps will resolve conflict in Git-**
    - Identify the files that have caused the conflict.
    - Make the necessary changes in the files so that conflict does not arise again.
    - Add these files by the command git add.
    - Finally to commit the changed file using the command git commit.
     
## 2.7. What is the difference between the 'git diff' and 'git status'?
<a id="markdown-What%20is%20the%20difference%20between%20the%20'git%20diff'%20and%20'git%20status'%3F" name="What%20is%20the%20difference%20between%20the%20'git%20diff'%20and%20'git%20status'%3F"></a>
  - **'git diff'** depicts the changes between commits, commit and working tree, etc. whereas **'git status'** shows you the difference between the working directory and the index, it is helpful in understanding a git more comprehensively. 'git diff' is similar to 'git status', the only difference is that it shows the differences between various commits and also between the working directory and index.
   
## 2.8. How will you know in Git if a branch has already been merged into master?
<a id="markdown-How%20will%20you%20know%20in%20Git%20if%20a%20branch%20has%20already%20been%20merged%20into%20master%3F" name="How%20will%20you%20know%20in%20Git%20if%20a%20branch%20has%20already%20been%20merged%20into%20master%3F"></a>
  - To know if a branch has been merged into master or not you can use the below commands:
    - **`git branch --merged`** : It lists the branches that have been merged into the current branch.
    - **`git branch --no-merged`** : It lists the branches that have not been merged.
      
## 2.9. Explain the difference between reverting and resetting.
<a id="markdown-Explain%20the%20difference%20between%20reverting%20and%20resetting." name="Explain%20the%20difference%20between%20reverting%20and%20resetting."></a>
  - Git reset is a powerful command that is used to undo local changes to the state of a Git repository. Git reset operates on "The Three Trees of Git" which are, Commit History ( HEAD ), the Staging Index, and the Working Directory.
  - Revert command in Git creates a new commit that undoes the changes from the previous commit. This command adds a new history to the project. It does not modify the existing history.

## 2.10. What is git cherry-pick?
<a id="markdown-What%20is%20git%20cherry-pick%3F" name="What%20is%20git%20cherry-pick%3F"></a>
  - The command git cherry-pick is normally used to introduce particular commits from one branch within a repository onto a different branch. Another common use is to forward- or back-port commits from a maintenance branch to a development branch. This is in contrast with other ways such as merge and rebase which normally apply many commits onto another branch.
    
    - **Example :**
      ``` 
      git cherry-pick <commit-hash>
      ```
