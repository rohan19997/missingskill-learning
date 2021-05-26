# Git

### <span style="color:#FFA400">**Introduction:-**</span>
-  git is an open source distributed version control system.
- we can do all the basic local git operations creationg or cloning a repository, making changes, staging and committing those changes and viewing the history of all changes the repository has been through.
- process where multiple team can work with same repository called collboration.
- atleast one developer work at time.


***
### <span style="color:#FFA400">**Commands:-**</span>

| command | description |
| --------| ----------|
| git init . | it create empty repository |
| git add | add a file |
| git status | shows the current status of the git |
| git log | history of git |
| git commit | added new file or updated  file to git |
| git diff | shows the status before commit |
|git show | show the actual history of commited file. |
| git branch | creating new branch |
| git checkout | switching the branch |
|git  checkout --<filename> | to recover  the file |
| git merge | all  the  file of  branch  merge with another branch |
| git stash |  used for  backup code |
| git stash pop | to bring back changes to the repository |
| git stash list |  to check some changes | 

***
### <span style="color:#FFA400">**Gitlab:-**</span>
- gitlab  are services that provides remote access to git repository.
- gitlab is a self hosted git repository management system.
***
### <span style="color:#FFA400">**Create a project:-**</span>
>git init .

 >git remote add origin https:......

>git add .

>git commit -m "---"

>git push origin master
***
### confict:- 
- two separate branches have made odits or when a file has been deleted in one branch but edited in other .
- it helps to loosing your works and update a file.

### if git rejected message :-
- that means remote branch ahead then local branch then we used 
>git pull origin master
