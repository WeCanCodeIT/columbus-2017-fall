# Guide to initializing git repositories and maintaining them

## Setting Up Local and Remote Repositories

1. Create a project in Eclipse `give-it-a-name-in-kebab-case`.

1. Create a class: `MakeSureToProperlyNameIt`.

1. Go to your command line (Git-bash) navigate to your project directory. (i.e. `~/wcci/default-workspace/your-projects-directory-name`)

1. In your command line, execute the command `git status`. This should return an error. If it doesn't you have a git repository set up in a parent directory of your current one.

1. Now create a git repository in your project directory: `git init`.

1. With a new repository initialized, re-check the status of your project: `git status`. This will show you all the untracked files inside of your repository.

1. Now it's time to track your files so they will be included in your commit. A good practice is to commit often so you should be adding everything each time. The command for which is: `git add .`.

1. `git status` again. All of your files should have changed color from red to green.

1. Now, with your green files, you are ready for your commit: `git commit -m "Add a descriptive message here so you can reference it later"`.

1. With all of your changes committed, you're ready to push them up to your remote repository: `git push`

1. Uh oh. You got a fatal error. This is because we don't have a remote repository connected to our local repository yet. Let's do that next.

1. In your browser, navigate to [Github](https://www.github.com), hit the plus sign in the top right corner and create a new repository.

1. Name this new repository the same thing that your project directory is named (i.e. your-projects-directory-name). Copy and paste to minimize the possibility of typos. You shouldn't change anything else in this window.

1. Push the button at the bottom ***Create repository*** to create new repository.

1. On this next page, there are two lines of code under **…or push an existing repository from the command line**. Copy these and paste them to your command line (`<ctrl> + <shift> + <V>`). Push `<enter>` to submit the final line.

1. Your local repository and remote repository are now connected.

1. If you go back to your browser and hit the **refresh** button. You will see your project files are now housed inside of your remote repo.

## Pushing Future Changes from Local to Remote

So you have changes now and you're ready to push them up. Let's get started.


1. First, navigate to your command line and execute `git status`. This should produce some untracked files. That's good. Let's get them tracked.

1. Track your files with `git add .`

1. Execute a `git status` again to double check that everything is being tracked.

1. Now commit your changes: `git commit -m "Another descriptive message to let you/other devs know what happened since the last change"`.

1. Now it's time to push. You don't need the two lines you used from your first push this time. The command for all pushes after the first one is: `git push`. This is because your local and remote repos are connected and mapped to each other. This command just tells the local to use that path and push the new information to it.

1. In your browser, navigate to [Github](https://www.github.com) and then your project repo. You should see the current version of your project housed in your remote repo now.
