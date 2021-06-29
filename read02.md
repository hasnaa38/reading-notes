# read 02 

In this file a summary of *read 02 - Git tutorial* will be provided. Click [here](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/) to read the original article, the summary is only up to *Seeing Your Remote* section. 

# Git tutorial
### Version control
Each time a coder commits an edit to a file, a new version of this file will be created. Version control is a system that allows coders to review and skim through the various versions of repository files. 
It allows coders to track changes, compare versions, and revert to a previous version if needed.  

### what is Git 
Git is an open-source version control system software. It tracks every single change applied to a file and/or directory and stores snapshots of all the versions of them.

Git should be installed on your machine in order for you to be able to use it. After the installation, you can start using it even if you were offline using any command line tool you have. Git has multiple GUIs (Graphical User Interface), however, using a command line tool is assumed throughout this tutorial. 

### Main Git commands 

- `git clone` to clone an already existing remote repository from a server (e.g. from GitHub) to Git using the repository's URL. 
- `git commit -m “add description”` to commit (=save) the changes you have made on this file/repository.
_**Note**_ committing changes is storing data the database. Without committing changes the modifications will not be stored in the database. 
- `git push origin main` to push (=upload) the new version of the repository from the local machine to the remote repository -the one on the server-.
_**Note**_ you don't have to paste the URL of the repository here since Git has saved it in **origin**. 
- `git status` to see information regarding the changes. 
- `git add .` to track all the repository files. 

### Steps 
The following are the most basic steps to modify a repository from GitHub: 

1. Get the repository's URL from GitHub. It will have the following format: 
https://github.com/username/repository-name.git 
2. Clone the repository: `git clone URL` 

![Figure .1](https://i.ytimg.com/vi/DhD0HkOkTYM/maxresdefault.jpg) 
Figure .1 illustrates an example of step1. 

3. Apply your modifications  
4. Commit changes: `git commit -m “add description”`
5. Push this version from local to GitHub: `git push origin main`

![Figure .2](https://ma.ttias.be//wp-content/uploads/2015/12/git_push_deploy-685x275.png)
Figure .2 illustrates an example of steps 4 and 5. 

