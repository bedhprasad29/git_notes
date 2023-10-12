# GIT
## _All about Git in One Place_

[![N|Solid](https://res.cloudinary.com/practicaldev/image/fetch/s---YzLIbj---/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/i/ka0rfekqburijjrb9yoh.png)](https://github.com/bedhprasad29/git_notes)

Git is a distributed version control system essential for software development, enabling developers to track changes, collaborate on code, and manage multiple versions efficiently by utilizing features like branching, merging, and remote repositories.

## Create Git Repository
1) Login to Git
2) Click on the "+" icon in the top right corner of the GitHub website.
3) From the dropdown menu, select "New repository."
4) Repository Configuration:
Fill in the repository name, a description (optional), and choose between making it public or private.
You can also initialize the repository with a README file, add a .gitignore file, and choose a license.
5) Click the "Create repository" button.

## Create Personal Access Token
1) Click on your profile picture in the top right corner. From dropdown select _Settings_
2) From left sidebar, click on "Developer settings."
3) Then Select Personal access token -> Tokens (classic)
4) Generate New Token (Generate new token (classic))
5) Select Name of Token, then Give Expiration (Recommended 90 days)
6) Select scopes whichever required.

## Commands

#### To Push Folders From Local PC to GitHub
Notes : 
1) Create a new git repository and have HTTPS or SSH link with you.
2) You should have git username and Token(Explained in _Create Personal Access Token Section_).
```sh
git init 
git add .
git commit -m "My first commit message"
git status
git remote add origin <repository_url>
git push origin master –-force 
(If asked, enter username then in password enter personal access token)
```

#### Branch Related

To __Create a New Branch__ : 
```sh
git checkout -b <branch_name>
or
git branch <branch_name>
```

To __Checkout to different Branch / Switch Branch__ : 
```sh
git checkout <your_branch_name>
or
git switch <your_branch_name>
```

To __List All Branches__ : 
```sh
git branch (Lists all local branches).
git branch -r (Lists all remote branches).
git branch -a (Lists both local and remote branches).
```

To __Fetch/Pull all Branches from Remote__ : 
```sh
git fetch origin  (Fetches all changes from the remote repository).
git pull origin <branch_name> (Pulls the specified remote branch into your local branch).
```

To __Push Branches to Remote__ : 
```sh
git push origin <branch_name>
```

To __Checkout to Last Branch__ : 
```sh
git checkout -
```

To __Rename Branch__ : 
```sh
git branch -m <old_branchname> <new_branchname>
```

To __View Branch History__ : 
```sh
git log   (To display All details)
git log <branch_name>  (Shows the commit history of a specific branch).
git log --graph --oneline --all  (Displays a graph of the commit histories).
```

#### Stash Related
Git stash is a command that allows you to temporarily save and set aside changes in your working directory without committing them.

To __Stash your changes__ : 
```sh
git stash       (To keep aside your modified changes)
git stash -u    (To keep aside your untracked + modified changes)
git stash save "Description" (Stash your changes with specific description)
```

To __List your Stash__ : 
```sh
git stash list
```

To __Apply your Stash Changes to Working Directory__ : (This won't remove your stash from stash list)
```sh
git stash apply  (Applies most recent Stash)
git stash apply n  ((n is specific stash number) Applies particular Stash changes).
```

To __Apply your Stash Changes to Working Directory__ : (This will remove your stash from stash list after applying)
```sh
git stash pop  (Applies most recent Stash)
git stash pop n  ((n is specific stash number) Applies particular Stash changes).
```

To __Delete Stash__ : (This will remove your stash from stash list)
```sh
git stash drop  (Deletes most recent Stash)
git stash drop n  ((n is specific stash number) Deletes particular Stash).
git stash clear  (Removes all stash from List)
```

To __Create a Branch From Stash__ : (This will create new branch with stash changes)
```sh
git stash branch <branch_name> (Creates from latest Stash)
git stash branch <branch_name> Stash n ((n is specific stash number) Creates from mentioned Stash)
```

#### Check Difference in Code in terminal

```sh
git diff  (To check differences between the working directory and most recent commit.)
git diff --staged  (To check changes in your staged code in working directory)
git diff --color-words   (Highlights the differences in color)
``` 

#### Remove all Changes available in working directory

```sh
git reset --hard
or 
git reset --hard HEAD && git clean -fd  (Also cleans Untracked Changes)
``` 

#### Remove GIT from packages
Sometimes We need to remove git from packages which are already initialized or those which are already available in github.

```sh
rm -rf .git
``` 

#### Revert Commited Changes
_For codes you already commited but not yet pushed to remote._
Delete the most recent commit, keeping the work you've done
```sh
git reset --soft HEAD~1
``` 

Delete the most recent commit, destroying the work you've done
```sh
git reset --hard HEAD~1
``` 

#### Tag Version to your repository
To tag the changes to deploy (First tag version then push the tag).
```sh
git tag v3.2.0  (v<version_number>) then
git push --tags
``` 

#### Cherry-pick commits
Cherry-pick is a command used to select and apply specific individual commits from one branch to another.

To pick the changes form one commit to current branch and use it in your working directory.
```sh
git cherry-pick <commit_id> -n
```

To pick the changes form one commit to current branch and merge it to remote (Be careful using this as this will direcly create commit to remote)
```sh
git cherry-pick <commit_id>
```

To cherry-pick multiple commits 
```sh
git cherry-pick <commit_id1> <commit_id2> <commit_id3> 
```