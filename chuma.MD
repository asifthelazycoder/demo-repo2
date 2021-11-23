# Git

## SSH Keys

* To establish a connection between a remote repository and our local machine, we need to generate SSH keys.
 
* Command for generating ssh key:

  ```ssh-keygen -t rsa -b 4096 -C "masif2002@gmail.com"```

       -t &rarr; type of encryption  
       -b &rarr; strength of encryption  
       -C &rarr; email address  

> two files will be generated
> key	  | private key, which will be used to show github that you are the owner of the public key.
> key.pub | public key, which you need to physcially add to GithHub under the SSH section

## Git Commands

    `git clone [SSH link]`  
Clones the remote repository into your local machine
* git add < filename > | Tracks the file (tracks the changes you've made)
* git add .            | Means it tracks all the files that have not been tracked 
* git status           | Displays the status of the files. 
* git commit -m "commmit title" -m "some description" | Commits the changes (save changes locally)





two files will be generated
key	| private key, which will be used to show github that you are the owner of the public key.
key.pub | public key, which you need to physcially add in github in SSH section

git push origin master | origin is where the git repo is cloned from... so git understands to push it to the repo originally where it was cloned from

git init | initializes git
git remote add origin <link from github with SSH> | connects to the repo on github

git remote - v | Shows remote repos connected

git push -u origin main | -u sets default push location to origin main branch, so you can stop with 'git push' :)

git commit -a | adds a modified file and commits it (only works with modified , not new ones) 
git commit -am "title" -m "desc" 

Step by step:
1. git clone
2. Make changes
3. git status
4. git add
5. git commit
  	
__________________
Branching

git branch | to check the branches available in repo
git branch -d <branch_name> | To delete a branch
git checkout -b <new_branch_name> | To create a new branch
git checkout <branch_name> | To switch to a branch

git diff | shows the diff in code after changing but before tracking
git diff <branch_name> | to get the difference in code between two branches OR to get a comparison bw 2 different version of the code

git pull origin master | pulls the merged master file from the remote repository to the local machine

git merge master 

git reset | resets all the changes in all the files that have been tracked
git reset <filename> | does the same with the filename which has been tracked but not committed
git reset HEAD~1 | undoes the commit.. What actually happens is that it resets the pointer which is currently pointing head to head-1 

git log | gives youu the log of (all) the commits made
git reset <hashkey> | resets to the commit with the hash specified. (hashkeys of commits can be found in git log)
git reset --hard <hashkey> | resets to the specified commit and also deletes the commits after the current one
 

Links:
Generating SSH Key: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

Gitlens for vscode

49:50 merge conflicts


#ls -la | it is like dir which also lists the hidden files in the current folderi
MD Syntax:

# For header line

## For subheader line
