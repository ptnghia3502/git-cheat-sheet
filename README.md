<div align = "center">

# Git Cheat Sheet

This repository is a collection of syntax, commands about git. </br>
This cheat sheet contains 50 commonly used git commands.
> 👌 Feel free to use my repository and star it if you find something interesting 😄

</div>
</br>

![Git Cheat Sheet](./git-cheat-sheet.png)
</br>

## 📔 Git Commands Tutorial
* ### Setup Git and first commit to repo
  * **Download/Install** </br>
    Download Git from this link: [Git - Downloads](https://git-scm.com/downloads) </br>
    After the file is downloaded, install it in the system. </br>
    Once installed, select Launch the Git Bash, then click on finish. Or right-click somewhere on desktop and choose Git Bash Here. </br>
    The Git Bash Console will be launched. </br>
    To check Git is installed or not, or check version, use this command:
    ```
    $ git --version
    ```
  
  * **Setup** </br>
    Set the name and email that will be attached to your commits and tags </br>
    ```
    $ git config --global user.name "ptnghia3502"
    $ git config --global user.email "ptnghia3502@gmail.com"
    ```
    </br>
   
  * **Starting a Project with Git** </br>
    Create a local repo (omit <directory> to initialise the current directory as a git repo) </br>
    ```
    $ git init
    ```
    Or download existed repo </br>
    ```
    $ git clone <url>
    ```
    </br>

  * **Make a Change** </br>
    Add a file to staging or stage all files (recommend)</br>
    ```
    $ git add <file>
    $ git add .
    ```
    Commit all staged files to git </br>
    ```
    $ git commit -m "commit message"
    ```
    </br>
    
  * **Push to repo** </br>
    If you create a local repo, you need to create new reposioty on your GitHub </br>
    On your GitHub profile, choose Repositories, click New, set name and description for your repo, then Create Repository </br>
    Get the HTTPS URL of your repo (Example: `https://github.com/ptnghia3502/example.git`) </br>
    Remote your local repo to repo on Github and push your content: </br>
    ```
    $ git remote add origin <url>
    $ git push -u orgin master
    ```
    If you clone repo from somewhere, just use `git push`, it will auto push to repo where you clone from.
    ```
    $ git push
    ```
    </br>
    
  * **Quick Tip from GitHub** </br>
    When you create new repository on GitHub, it will show fast command line </br>
    Or create a new repository on the command line: </br>
    ```
    $ git init
    $ git add .
    $ git commit -m "first commit"
    $ git branch -M master
    $ git remote add origin <url>
    $ git push -u origin master
    ```
    Or push an existing repository from the command line: </br>
    ```
    $ git remote add origin <url>
    $ git branch -M master
    $ git push -u origin master
    ```

* ### Create and merge branche
  * **Branches** </br>
    List all local branches. Add `-r` flag to show all remote branches, `-a` flag for all branches </br>
    ```
    $ git branch
    ```
    Create a new branch </br>
    ```
    $ git branch <new-branch>
    ```
    Switch to a branch & update the working directory </br>
    ```
    $ git checkout <branch>
    ```
    Create a new branch and switch to it (combine of 2 above, I recommend use this) </br>
    ```
    $ git checkout -b <new-branch>
    ```
    Delete a merged branch, and Delete a branch, whether merged or not </br>
    ```
    $ git branch -d <branch>
    $ git branch -D <branch>
    ```
    Add a tag to current commit (often used for new version releases) </br>
    ```
    $ git tag <tag-name>
    ```
    </br>
    
  * **Merging** </br>
    Merge branch a into branch b. Add `--no-ff` option for no-fast-forward merge </br>
    ```
    $ git checkout b
    $ git merge a
    ```
    Merge & squash all commits into one new commit </br>
    ```
    $ git merge --squash a
    ```
    </br>

* ### Another Commands
  * **Undoing Things** </br>
    Move (&/or rename) a file & stage move </br>
    ```
    $ git mv <existing_path> <new_path>
    ```
    Remove a file from working directory & staging area, then stage the removal </br>
    ```
    $ git rm <file>
    ```
    View a previous commit (READ only) </br>
    ```
    $ git checkout <commit_ID>
    ```
    Create a new commit, reverting the changes from a specified commit </br>
    ```
    $ git revert <commit_ID>
    ```
    Go back to a previous commit & delete all commits ahead of it (revert is safer). Add `--hard` flag to also delete workspace changes (BE VERY CAREFUL) </br>
    ```
    $ git reset <commit_ID>
    ```
  * **Review your Repo** </br>
    List new or modified files not yet committed </br>
    ```
    $ git status
    ```
    Show changes between two commits </br>
    ```
    $ git diff <commit1_ID> <commit2_ID>
    ```
    
