### Deploying a static website to GitHub Pages using npm

+ Have nodejs installed.
+ You can check version by using `npm --version`
+ Generate package.json using `npm init -y` The y flag is to give yes answer for all the questions asked.
+ Install gh-pages
  + `npm i gh-pages`
+ Add following values to your package.json file
  + "homepage":"https://Excelligence.github.io/SellerVarsity"
+ Now add a script to deploy to gh pages 
  + "deploy":"gh-pages -d <folder to be deployed> "
+ Now make a new repository in github
+ create .gitignore file and add files/folders to be ignored
+ Push the repository to github
+ Now run `npm run deploy`
+ Now when published is seen goto your github settings and go to the url