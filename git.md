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
  
