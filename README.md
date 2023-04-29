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
* **Setup** </br>
  Set the name and email that will be attached to your commits and tags </br>
  ```
  $ git config --global user.name "Danny Adams"
  $ git config --global user.email "myemail@gmail.com"
  ```
   </br>
   
* **Starting a Project with Git** </br>
  Create a local repo (omit <directory> to initialise the current directory as a git repo) </br>
  ```
  $ git init <directory>
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
