# deploy_vue

This is very simple not good looking small project just to try to deploy vue + vite + router App to GitHub Pages.
In terms of Vue it means once we build our Vue project, we can serve that static index.html file. Easiest way to do this is create a gh-pages branch which contein a build folder (/dist).

### First step: create our project repo

in GitHub create a new repository whith name 'deploy-vue'

next,in Terminal go to folder project and initialized empty Git repository
 ```sh
 git init
```

 git add .
 
 git commit -m "first commit"
 
 git branch -M main
 
 git remote add origin https://github.com/Festival3224/deploy-vue.git
 
 git push -u origin main

 after puph we can see our repo in GitHub

 ### Let's Start Deploying!

I'm going to deploy to https://<USERNAME>.github.io/<REPO>/. So, I have to change my Vite config! Set base to '/<REPO>/' in vite.config.js file:

```sh
 base: 'deploy-vue',
```
### Now I can build my Vite project!

```sh
npm run build
```

### Awesome - time to push to gh-pages
```sh
 git add dist -f
```
 We need -f, couse Vite's default .gitignore ignores /dist !
 
Next:
```sh
 git commit -m "adding dist"

 git subtree push --prefix dist origin gh-pages
```
 
!!! There was an error message: 'subtree' is not a git command. See 'git --help'.
Solved by command "dnf install git-subtree" !!!

```sh
git push using:  origin gh-pages
.......
mambo-jumbo -> gh-pages
```

this step created gh-pages, a subtree of our master branch
 
 
 
