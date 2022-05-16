# Git commands

# GIT
```
git init 
```

Initialize an empty git repository

```
git status 
```
 
Check the status of any change in repository
```
git add .
``` 
Add all the changes to git repository you can also add files individually
```
git commit -m "{message}" 
```
Commit the change with message 
```
git log 
```
Displays all commits that are made 

```
git stash
``` 
Save the changes in background used for data which we don't wat to commit but want to save 
 ```
 git stash pop 
```
Brings stashed data back
```
git reset {commit id} 
```
Reset the branch to given commit 

---------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------

 
 
- GITHUB 
```
  git remote add origin {url of repository} 
```
Adds remote repository url with origin name  for working with online repository
``` 
   git remote -v 
```
Check the remote repositories URL 

---------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------
  
  
- BRANCHES
```
  git branch  {Branch Name}
```
 For creating new branch 
 ```
  git checkout {branch name} 
```
Moving head to selected branch now commits will be added to new branch 
  ```
   git merge {branch to be merged with main}
```
Merges desired branch with main


---------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------

- PULL & PUSH
``` 
  git push origin master 
```
Pushing changes into online origin named repository's master branch 
```
  git pull origin master 
```
Pulling  changes from online origin named repository's master branch 

---------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------

 
- LINK PC WITH GITHUB ACCOUNT WITH THE HELP OF SSH.


--Create ssh keys for account as following .
```

ssh-keygen -t ed25519 -C "your_email@example.com"
```
          or
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com" 
```

After this please setup further process by entering required data like key name and passpharese.

After that you have two keys one private key and another public key in .ssh folder 

--Add private key to ssh agent as following:-
```
 ssh-add ~/.ssh/key_name

```

--Link key with GITHUB account.


 for linking ssh key to github account copy the content of public key {key_name.pub) data and copy it to ssh keys in your github account.
 
---------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------

- Two GITHUB account in one PC

-- Create Two public and private key  pair for each GITHUB account and link both with ssh keys {refer step above}

-- create a config file in ./ssh directory
directory should look like this :- 

```
.ssh/
   ├─ config/
   ├─ key_1/
   ├─ key_1.pub/
   ├─ key_2/
   ├─ key_2.pub/
   
```  
-- configure file as following
```
 #First Account 
Host github.com
   HostName github.com
   User git
   IdentityFile ~/.ssh/key_1

 #Second account
Host github.com1
   HostName github.com
   User git
   IdentityFile ~/.ssh/key_2

```




-- NOTE: while adding remote for first and second account please use following syntex

Account 1 :-
```
 git remote add origin git@github.com:abc/xyz.git
```

Account 2 :-
```
 git remote add origin git@github.com1:abc/xyz.git
```

---------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------------------------------


- Forking and Pull Request


--Forking is a way to contribute into  public open projects   it clones public repository into users account so user can make changes and contributions to the project without affecting the main project.


--when we want to include changes made by us into pulic repository or project  we make a pull request to the user of main public repository  to accept changes . Only after accepting and merging pull request changes are visible. 




























  
