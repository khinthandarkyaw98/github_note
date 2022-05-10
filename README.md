# github_note
about_github
https://www.jcchouinard.com/get-started-with-github/

https://www.jcchouinard.com/add-a-file-to-github-with-git-bash/

https://articles.assembla.com/en/articles/1136998-how-to-add-a-new-remote-to-your-git-repo

Create a folder in your local computer. 
Open Git Bash.
Enter the location of the created folder using cd command on Git Bash.

cd 'location' (if the folder's name includes whitespaces)
or 
cd location ( if there is no whitespace in the name of the folder)

Then copy the link of the repo on GitHUB.
Come back to Git Bash and write the following command.

Step 1 : git clone Repo_LINK

This will create a repo folder in your local computer.

Then paste the file you want to add to the github in the repo folder in your local computer.

The file location you pasted on your local repo must match the location on Git Bash in which you will write 'git add' command! 
Else don't forget to define the location with cd again on Git Bash!

```git log``` can be used to show the previous commit messages. 

```q``` or ```clrt+z``` can be used to tackle 'END' display.

```git difftool HEAD``` is used to see the changes made.

```
- uncommited changes
```

```git checkout -- filename```can be used to undo the lines in the file.

```git checkout -- .``` can be used to undo all the changes in all files.

Then go to Git Bash and write the following command.

Step 2: git add 'file.type'

Step 3: git commit -m 'added file type or write a comment'

Step 4: git push origin master

Then check your GitHub.

You can remove by using the following command!

Step 5: git rm filename

Step 6: git commit -m 'removed the file'

Step 7: git push origin master

However, I prefer using GitHub's web interface!!!


