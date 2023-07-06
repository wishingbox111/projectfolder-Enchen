### projectfolder-Enchen


# Introduction to basic Git Commands 
Here are some of the commonly used Git commands to be used in Bash or Powershell in windows.

*To Start a new repo*
- create a repo in Github manually


*To turn an existing directory into a git repository*
 - `$ git init`



*To download the files from Github repo*
- `git clone` is used for just downloading exactly what is currently on the remote repository and saving it in your machine's folder where that project is placed. (Only one time) 
- `git fetch` is the command that tells the local repository that there are changes available in the remote repository without bringing the changes into the local repository.
- `git pull` downloads the changes and merges them into your current branch. (Can be multiple time if there is new changes on the branch in the repo). 
  
*To use local file to push into Github Repo*
- `git add .` Stage the all the file for commit to your local repository by the following command.
- `git commit -m` After creating changes on README file and to commit the file that you’ve staged in your local repository.
- `git push`  1)Push the changes in your local repository to GitHub.
              2)A pull request is an event in Git where a contributor asks a other member of a Git repository to review code they want to merge into a project.
- `git push origin main` 	Push the changes in your local repository to GitHub.

  *To check*
- `git status` List which files are staged, unstaged, and untracked
  
### Git Branch (Creating and Going to Branch)

- `git branch` create new branch 
```
        git branch feature2
```
- `git checkout` Change to the new branch 
```
        git checkout feature2
```
- `git checkout -b` create new branch and change to the branch (combination of the two code above)
```
        git checkout -b <new-branch-name>
```
create the changes on local file - Execute by steps
- `git add .`
- `git commit -m “Comment of the changes”`
- `git push --set-upstream origin <new-branch-name>` - note <> should not be in the code
- `git push`

*Once you merge the codes using the browser (console)
you can delete the branch (option available after merging)
when you check with `git status`, CLI/powershell is still in the deleted branch*

- `git checkout main` to move back to main branch
- `git pull` as the main branch would have changed from last merge. To pull the changes into local folder.

  

----------


  
  ## Annex
 ***See Git download instructions for windows here:**
  > https://kinsta.com/knowledgebase/install-git/
 
 To configure and connect to git repository:
```
  $ git config --global user.name "[name]"      
  ^"Sets the name you want attached to your commit transactions"
  $ git config --global user.email "[email address]"
  ^"Sets the email you want attached to your commit transactions"
  $ git config --global color.ui auto
  ^"Enables helpful colorization of command line output"
  ```


  
  
  > Do note that if you follow the instructions for downloads below, cd into the folder in Desktop same name as Repo in Git. try `git init`,`git add .` and `git commnit -m "push"`, and then `git push`, by the last step the program should ask you for credentials (which is to be done once). If it did not happen. Connect from HTTPS or SSH shown in Annex. Instructions are yet to be tested by myself and is still a work in progress. 
  
  
  ***Creating SSH Keys when credentials manager in downloaded Git is not working**
  
  - go to github.com > settings > SSH & GPG Keys > New SSH Key > Add SSH Key
  - remove existing folder 
  - git clone <SSH URL>
  - git push https://<PERSONALACCESSTOKEN>@github.com/<YOUR git username>/<your repo name>.git

### Resource
- Dillinger
- https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet
- https://training.github.com/
- [GitHub Flow Cheatsheet] https://enterprise.github.com/downloads/en/github-flow-cheatsheet.pdf
- Work based on -cloud-3.1-introduction-to-git-i/assignment.md

**To read:**
-  [Git Flow] https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow
- [GitHub Flow] https://docs.github.com/en/get-started/quickstart/github-flow
- [Trunk based development] https://cloud.google.com/architecture/devops/devops-tech-trunk-based-development
- [GitFlow vs GitHubFlow] https://www.geeksforgeeks.org/git-flow-vs-github-flow/ (Optional Read)


