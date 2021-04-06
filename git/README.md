# The basics of git and GitHub
This document contains the most important HowTos of my regular workflow with git/GitHub
## Clone an existing GitHub-REPO into an _(empty)_ folder via git-Bash
```
// navigate to the desired local folder and launch "Git Bash here" ... then type:
git init
git remote add origin [my-repo]
git fetch
git checkout origin/[master] -ft
// instead of [master] I might have to use [main] or whatever the name of the main branch is :-)
```
## Push the local branch to github
This will only work, if the local REPO has been setup as described above!
```
git push

// in case you are on a new branch (that is yet unkown on GitHub)
// you will get clear instructions on what to do :-)
$ git push
fatal: The current branch NewBranch has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin NewBranch
```

## Connect a local project to a NEW _(empty)_ GitHub-REPO
If you have already setup a new project in your local development-environment, and feel it's time to start putting it up on GitHub ... here's how it can be done
* Make your local folder a git-repo
  * ```
  git init
  git add [at least one file]
  git commit -m "first commit"
  git branch -M main
  ```
* Open the project-folder with the ATOM-editor and commit the rest of the files and folders
* Setup **.gitignore** _(if necessary)_
  * See details here: https://docs.github.com/en/github/getting-started-with-github/ignoring-files
* Login to your GitHub-account and create a new REPO _(both Public or Private will work)_
  * **Don't** initialize any of the proposed files _(README.md / License)_
  * This makes sure, that the GitHub-REPO will be empty!
* Open Git Bash in the root folder of your local repo
  *  ```
  git remote add origin https://github.com/[YOUR-REPO].git
  git push -u origin main
  ```
