Bash history search, partial + up-arrow
---
  
  Put the following lines in your ~/.inputrc:

    ## arrow up
    "\e[A":history-search-backward
    ## arrow down
    "\e[B":history-search-forward
