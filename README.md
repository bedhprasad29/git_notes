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
1) Click on your profile picture in the top rights corner. From dropdown select _Settings_
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
```˝