# Git Commands
## _All Required Git Commands in One Place_

[![N|Solid](https://res.cloudinary.com/practicaldev/image/fetch/s---YzLIbj---/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/i/ka0rfekqburijjrb9yoh.png)](https://github.com/bedhprasad29/git_notes)

Git is a distributed version control system essential for software development, enabling developers to track changes, collaborate on code, and manage multiple versions efficiently by utilizing features like branching, merging, and remote repositories.

## Create Personal Access Token
Click on your profile picture in the top right corner.
It will give dropdown, from dropdown select _Settings_
From left sidebar, click on "Developer settings."
Then Select Personal access token -> Tokens (classic)
Generate New Token (Generate new token (classic))
Select Name of Token, then Give Expiration (Recommended 90 days)
Select scopes whichever required. If no idea then select all.

## Commands

To Push Folders From Local PC to GitHub
Notes : 
First create a new git repository and have HTTPS or SSH link with you.
Second have git username and Token(Explained in _Create Personal Access Token Section_) with yourself.
```sh
git init 
git add .
git commit -m "My first commit message"
git status

```
