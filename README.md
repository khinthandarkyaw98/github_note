# github_note
about_github

If you cannot push to repo from terminal (passward access is denied), use token. Refer to this [blog-post](https://ginnyfahs.medium.com/github-error-authentication-failed-from-command-line-3a545bfd0ca8).

https://www.youtube.com/playlist?list=PLeo1K3hjS3usJuxZZUBdjAcilgfQHkRzW

https://www.jcchouinard.com/get-started-with-github/

https://www.jcchouinard.com/add-a-file-to-github-with-git-bash/

https://articles.assembla.com/en/articles/1136998-how-to-add-a-new-remote-to-your-git-repo

#############################################


create a new repository on the command line

```echo "# text_description" >> README.md```

```git init```

```git add README.md```

```git commit -m "first commit"```

```git branch -M main```

```git remote add origin xxxxxx.git```

```git push -u origin main```


…or push an existing repository from the command line

```git remote add origin xxxxxx.git```

```git branch -M main```

```git push -u origin main```






#############################################

If you have already created the repo in your github, you can ocate the folder which has the similar name as that of your repo via terminal, follow these steps. 

   echo "# Neural_Networks" >> README.md
```git init```

```git add README.md```

```git commit -m "first commit"```

```git branch -M main```

```git remote add origin https://github.com/github_username/github_repo_name.git```

```git push -u origin main```

    
    # for test branch
    

    ```git checkout -b test    # creates a new branch named "test" and switches to it```
    
```git add .               # add any changes to the staging area```

```git commit -m "commit message"   # commit your changes```

```git push origin test    # push your changes to the remote "test" branch```

```git checkout main       # switch back to the "main" branch```

```git merge test          # merge the changes from the "test" branch into the "main" branch```

```git push origin main    # push the merged changes to the remote "main" branch```


<hr>

Create a folder in your local computer. 
Open Git Bash.
Enter the location of the created folder using cd command on Git Bash.

cd 'location' (if the folder's name includes whitespaces)
or 
cd location ( if there is no whitespace in the name of the folder)

Then copy the link of the repo on GitHUB.
Come back to Git Bash and write the following command.

Step 1 :  ```git clone Repo_LINK```

This will create a repo folder in your local computer.

After writing the code or lines in the file. 

Then go to Git Bash and write the following command.

Step 2: ```git add 'file.type'```

Step 3: ```git commit -m 'added file type or write a comment'```

Step 4: ```git push```

Then check your GitHub.

You can remove by using the following command!

Step 5: ```git rm filename```

Step 6: ```git commit -m 'removed the file'```

Step 7: ```git push``` 

---

>Undo for uncommitted changes

```git checkout -- filename```can be used to undo the lines in the file.

```git checkout -- .``` can be used to undo all the changes in all files.

---

## Commit

> Show the recent commit
```git show HEAD``` 
----
>Undo for committed changes

```git log``` is used to retrieve committed_id

```git revert committed_id ``` can be used to undo commited changes

---

> Try to avoid the following code as much as possilbe unless necessary.

```git reset --hard committed_id``` is used to restore back to where it was.

---

### Add Branch

> Check the branches 
```git branch``` 

> Create the branch
```git brannch branch_name```

>Go the branch
```git checkout branch_name```

You can write the above two closest code lines into one line.

>This will create the branch and checkout it at the same time.
```git checkout -b branch_name```

Make changes in the file.
Then svae it.

> Go staging space
```git add file_name```

> Add commit
```git commit -m "message"```

> Go to main branch to merge the files 
```git checkout main```

> Merge the brach to the base branch(main)
```git merge branch_name``` branch_name will be merged to the main

> Go checkout to the branch(copy) to push the branch
```git checkout branch_name```

> Then Push the branch from the branch_name to the Github
```git push --set-upstream origin branch_name``` git will push the branch the upstream which is Github

### Delete Branch

> Please checkout to the main first before deleting the branch
```git checkout main```

>When you are in the main or master branch, then you can the delete the branch you wish to.
```git branch -d branch_name``` or 
```git branch -D branch_name``` The latter is "force delete".

### Delete file
> Make sure the location in the folder where the file to be deleted is.
```git rm filename```

### Create folder
```mkdir folder```

### Create file
```touch filename```

#### To solve detached HEAD [Click HERE](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/git-push-new-branch-remote-github-gitlab-upstream-example)

### Changes in remote
If you made chages in remote(github), go to the location of this file in git bash with cd command and write ```git fetch origin main``` and
```git merge origin/main```

---

#### difftool

```git log``` can be used to show the previous commit messages. 
> show the difference between previous commit and new commit
```git difftool old_commit_id new_commit_id```

> HEAD is the recent commit_id. 

> HEAD~1 is the commit_id before the recent one.

> HEAD~2 is the the second commit_id before the recent one.

```git difftool HEAD HEAD~1``` show the difference between the recent one and the other before it.

```git difftool HEAD``` is used to see the changes made

---
### QUIT/ END

```:q``` or ```clrt+z``` can be used to tackle 'END' display.

```:wq``` is used when ```:q``` cannot be used. 

---
### IQNORE

```touch .gitignore``` created a file named '.gitignore' in the local repo

> open the file in the local repo and write the file name desired to be ignored
> if there are multiple files to be neglected,e.g 'a.exe', 'b.exe', then write ```*.exe``` in the '.gitignore' file.

### Wrong Language
#### .gitattributes

> If the Github describes the wrong language in the languages bar, create ```.gitattributes```
 in the local repo by using 
 ```touch .gitattributes``` . If it is desired to discard the python language,
 then simply use the following command.
 
 ```*.py linguist-detectable=true```
