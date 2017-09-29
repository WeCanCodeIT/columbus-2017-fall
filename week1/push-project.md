## Use this guide to push your first Eclipse project to GitHub

- Create a project in Eclipse called push-project
- Create a class in the project called Push
- Create a new Repository in GitHub called push-project and click the green **create new repository** button
- Remain on the Quick Setup page as we will need to copy the HTTPS link at the top 

- Open Git Bash and key in the following commands (hit enter after each command line below)
- `cd ..`    will back out 1 directory
- `ls`       will show available directories 
- `cd default-workspace/`  will allow you to access your Eclipse workspace directory 
- `ls` again to show an updated list of available directories (these should be your Eclipse projects)
- `cd push-project`
- `git remote -v`  probably won't do anything now
- `git init`  
- `git remote -v` probably won't do anything now
- `git add .`   this will take all contents inside of the Eclipse project
- `git commit -m "first commit" ` after you add your contents commit them to prepare for GitHub
- `git remote add orign [copy link from new GitHub repo here...remove the brackets]`
- `git push origin master`
- refresh your GitHub repo to update and see the changes

- make a change in your Push class
- in Git Bash type `git status`  you should see a modification
- add, commit and push this modification (you do not need to do git push origin master again)
- update your GitHub again notice the change? Click on the commits link. 

