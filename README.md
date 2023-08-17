# deploy_vue


### Compile and Hot-Reload for Development

```sh
npm run dev
```

This is very simple not good looking small project just to try to deploy vue + vite + router App to GitHub Pages.
in Terminal go to folder project and initialized empty Git repository
 ```sh
 git init
```

 git add .
 
 git commit -m "first commit"
 
 git branch -M main
 
 git remote add origin https://github.com/Festival3224/deploy-vue.git
 
 git push -u origin main

 ### Compile and Minify for Production

```sh
npm run build
```

 git add dist -f

 git commit -m "adding dist"

 git subtree push --prefix dist origin gh-pages
 
!!! There was an error message: 'subtree' is not a git command. See 'git --help'.
Solved by command "dnf install git-subtree" !!!

git push using:  origin gh-pages
.......
mambo-jumbo -> gh-pages
 
 
 
