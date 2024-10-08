```bash
# git tracking
Install-Module posh-git -Scope CurrentUser

Import -Module posh-git

######################################################

git init

# view 
ls -a
ls -Force

explorer .git

######################################################

# remove git
Remove-Item .git -Recurse -Force
rm -rf .git

git init

######################################################

# write file
echo hello > file1.txt

echo hello > file2.txt

######################################################

# status
git status

# add to the staging area
git add *.txt
# entire dir recursively
git add .

######################################################

# append to the existing file
echo world >> file1.txt

git add file1.txt

######################################################

# from staging area to snapshot of git
git commit 


# this will automatically open your VS code
# Short description
# Long description


git commit -am "Fix the bug that prevents users from signing up"
######################################################

# removing file (unix cmd)
rm file2.txt

# a change in local just happened
# file2 was removed from the local
# but file2 does still exist in the staging area
# you can check
git ls-files

# so you have to use git add to remove from the staging area as well
git add file2.txt

git commit -m "Remove unused code"

# or you can use direclty without writing rm(unix cmd) and (git add) separately
git rm file2.txt

git commit -m "Remove unused code"
######################################################

# renaming file name
# deletion and adding operations happened
# renaming is in both the working directory and the staging area
# deletion is only in the working directory
mv file1.txt main.js

git add file1.txt

git add main.js

# you can use directly
# to allow everything happens in both the working directory and the staging area
git mv main.js file1.js

######################################################

# *****************Make sure to write gitignore in UTF-8****************************

mkdir logs

echo log > logs/dev.log

git commit -am "add logs"

echo logs/ > .gitignore

git commit -am "ignore logs"

git ls-files

# remove logs dir only from the staging area
git rm --cached -r logs/

git commit -m "remove logs from staging area"

git status

git ls-files

#####################################################

# check status in details
# red represents working dir
# yellow represents staging area
git status -s


####################################################

# view differnces in staging area
git diff --staged

# view differences in working directory
git diff

######################################################

# view diff tool
git config --global diff.tool vscode

git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE"

git config --global -e

git difftool --staged

git difftool
######################################################

# view log
git log

git log --oneline 

git log --oneline --reverse

# quit
q

#show by index
git show xxxxxxx
######################################################

# unstage 
# step back from staging area to working directory
# undo git add and git commit
git restore --staged filename
######################################################

# discard local changes 
# removing to the previous snapshot of staging area to the working directory
git restore .

######################################################

# undo local untracked files
git clean -fd


######################################################

# stage back to previous version
# view the commit comment that you want to go back
# copy the index
git log --oneline

git restore --soucre=index README.md

git add .
git commit -m "restored"

git restore --soucre=index --staged README.md

######################################################
```