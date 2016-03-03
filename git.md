Setup
---

    git clone <repo>
  
clone the repository specified by <repo>; this is similar to "checkout" in
some other version control systems such as Subversion and CVS

Add aliases to your ~/.gitconfig file:

  [alias]
  
    st = status
    ci = commit
    br = branch
    co = checkout
    df = diff
    dc = diff --cached
    lg = log -p
    lol = log --graph --decorate --pretty=oneline --abbrev-commit
    lola = log --graph --decorate --pretty=oneline --abbrev-commit --all
    ls = ls-files

  # Show files ignored by git:
    
    ign = ls-files -o -i --exclude-standard

Create a .gitignore file

    touch .gitignore
    

Configuration
-------------

edit the .git/config [or ~/.gitconfig] file in your $EDITOR

    git config -e [--global]

sets your name and email for commit messages

    git config --global user.name 'John Doe'
    git config --global user.email johndoe@example.com

To view all options

    git config --list

show a diff of the changes made since your last commit

    git diff
  
show files added to the staging area, files with changes, and untracked files

    git status
  
  show recent commits, most recent on top.
    
    git log

show who authored each line in <file>

    git blame <file>
  
Adding / Deleting
-----------------
add <file1>, <file2>, etc... to the project

    git add <file1> <file2> ...

add all files under directory <dir> to the project, including subdirectories

    git add <dir>

add all files under the current directory to the project 
    
    git add .

remove <file1>, <file2>, etc... from the project
    
    git rm <file1> <file2> ...
  
remove all deleted files from the project
    
    git rm $(git ls-files --deleted)
  
Staging
-------

 add changes in <file1>, <file2> ... to the staging area (to be included in the next commit)
 
        git add <file1> <file2>
        
interactively walk through the current changes (hunks) in the working tree, and decide which changes to add to the staging area.

        git add -p
      
remove the specified files from the next commit

        git reset HEAD <file1> <file2> ...

Committing
----------

commit <file1>, <file2>, etc... using commit message <msg>

        git commit <file1> <file2> ... -m '<msg>'
  
edit the commit message of the most recent commit
  
        git commit --amend
  
redo previous commit, including changes made to <file1>, <file2>, etc...
        
        git commit --amend <file1> <file2> ...
  
Branching
---------

list all local branches
        
        git branch

list all remote branches
        
        git branch -r
  
create a new branch named <branch>, referencing the same point in history as the current branch

        git branch <branch>
  
delete the branch <branch>;   
  
        git branch -d <branch>
        

make the current branch <branch>, updating the working directory to reflect the version referenced by <branch>
  
        git checkout <branch>
        
Merging
-------

merge branch <branch> into the current branch

        git merge <branch>


merge branch <branch> into the current branch, but do not autocommit the result
  
        git merge <branch> --no-commit

Cherry-Picking
--------------

selectively merge a single commit from another local branch
        
        git cherry-pick [--edit] [-n] [-m parent-number] [-s] [-x] <commit>
  
Example: 
        
        git cherry-pick 7300a6130d9447e18a931e898b64eefedea19544

  
