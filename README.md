# mvmsAngular
This file have GIT Commands which can be use to work with GitHub using GIT.
Starting Git Process:
Go into the folder and fire up Git Bash and enter "git init"
Command: git init -> Is used to start track by GIT
Command: git status -> To check status of the Repository
Command: git log -> To check the log details of repository

Adding and Removing Files For Tracking:
Command: git add <File_Name1,File_Name2> -> Files to be tracked by GIT
e.g: git add PersonViewModel.cs
Command: git rm <File_Name1,File_Name2> -> Files to be removed from tracking

Discard Changes in Files: 
Command: git checkout <File_Name> -> To discard changes of file
e.g: git checkout PersonViewModel.cs

Commiting Changes:
Comamnd: git commit -m "Four Files are added" -> To commit the changes after adding the files

Adding and Removing Remote Repository Address
Command: git remote add origin "url" -> To add remote repository either from GitHub or TFS
e.g: git remote add origin https://github.com/wiqistar/reponame.git
Command: git remote -v -> To verify remote repository
Comamnd: git remote remove origin -> To remove the Origin if added using the "Remote Add Origin"
Pushing to remote repository:
Command: git push -u origin master -> to push files to remote repository

GIT Fetch-Merge For Updating Local Repository:
For Updating Local Repository but it will fetches the updates but don't apply on the local
repository
Command: git fetch origin master

For Updating the local repository after fetching the changes from the Remote repository 
merge should be done using merge command. In this way if there are any conflicts then can be resovled
and it is preferable to use Fetch-Merge instead of Pull because Pull fails in case of Conflicts

Command: git merge origin/master -> It will update the local repository updates brought by Fetch command

GIT PULL:
It is used when you are sure that there are no conflicts otherwise it will fail if there are conflicts

Command: git pull origin master -> It will bring updates and merge them into local repository

TWO Different Repositories – Allow-Unrelated-History
    For Syncing the changes that were among Local and Server copies while working with two different repositories. Because if there were files which are present at Server but not available locally then GIT throws error because of history in 

Command: git push -u origin master

To https://github.com/wiqistar/angularlearning.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/wiqistar/angularlearning.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Allow-Unrelated-History:

Comamnd:git pull origin master --allow-unrelated-histories -> it will enable Push commands by bringing the Files present at Remote Repo 
in this the problem goes away and we can use "Push"

