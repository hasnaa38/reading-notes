# Git Branches

## Adding and accessing branches using the terminal

1. To create a new branch:

```
git checkout -b branchName
```

To access an already existing branch:

```
git checkout branchNAme
```

2. Now you are in the branch, you can clone repositories, add directories and files and edit them, or do whatever you want as usual.

3. ACP to GitHub:

```
git add .
git commit -m "message"
git push origin branchName
```

## Pull request

Pull request can be done to replace the code in a branch with the code from a different branch/repo.
This can be done on GitHub by selecting *Pull Requests*, then creating a *new pull request*.
Be careful when choosing from where to where you want your code to go.

Each pull request should be accepted. If you were pulling code within your account, go to the intended reop/branch and select *Pull Requests*. In there you can find the request, view the changes, and accept it (merge) if you want.

## To update the repository on the local device

Any changes on online repositories won't be added to their version on the local device, which may cause errors while pushing from the device because they don't match. Therefore, every time you accept a pull request on GitHub, you should do the following on your local device terminal:

```
git pull origin branchName
```