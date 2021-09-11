# React Steps

## To create a React app

1. Go to the dir you want to create the app in, preferably the root `cd ~`
2. Run `npx create-react-app appName` and wait
3. Create an empty GitHub repo without ReadMe file
4. In the root of the React app, run the following commands:

* `rm -rf .git`
* `git init` (you can skip this two steps because git initialize it for me)
* `git add .`
* `git commit -m "first commit"`
* `git branch -m main` - we are changing the main branch from master to main because we are pushing to GitHub
* Two options:

for SSH: `git remote add origin git@github.com:userName /repoName.git`
for HTTP: `git remote add origin https://github.com/userName /repoName.git`
* `git push -u origin main`

We may need to use `npm i` to install dependencies

## Deploying the app on Netlify

1. Go to Netlify
2. Choose new site from git
3. GitHub --> the repo name
4. You choose the correct root branch (main or master)
5. All configurations will be done already (run command, public directory .... )
6. Go to site settings
7. Build and deploy (from sidebar)
8. Environment --> add variables
9. key : CI --> Value : false
10. save
11. Go to deploys (in the top navbar)
12. Trigger deploy button --> deploy site
13. Wait a minute
14. Click on preview button