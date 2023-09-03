## Install Git

Install Git on your computer, if you haven’t already.

Configure your Git account information to reflect your Github information.

#### Email

`git config –global user.email` _`your_email`_

#### (Optional) Name

`git config –global user.name` _`your_name`_

#### (Optional) Username

`git config –global user.username` _`your_username`_

## Clone Repository

In a terminal, navigate to where you would like to store this project.

In Github, on the top right-hand side, above the repository’s files, click on the “Code” button, and copy the URL under “HTTPS”.

In your terminal, enter `git clone` _`copied_url`_

You may run into an error that I did that says something along the lines of “filename too long”. To fix this error, open a terminal as an Administrator and enter `git config –system core.longpaths true` then try again.

Use the command `git status` to verify that you’re on the main branch.

## Create your own branch

Instead of working directly on the main branch, you’ll be working on your own separate branches for each feature you work on. When you finish that feature, you will push that up to the repository so that the rest of the team can review it before it’s merged into the main branch.

To create your own branch, use the command `git branch` _`branch_name`_ and then use either `git checkout` _`branch_name`_ or `git switch` _`branch_name`_ to switch from the main branch to your create branch.

Alternatively, you can create a branch and switch to it with this single command `git checkout -b` _`branch_name`_

If you use the `git status` command again, you should now be on your created branch.

You can also use the `git branch` command to view all other branches in your local git repo.

## Work on your stuff

Work on your feature as you normally would.

## Stage changes

When you’re finished with your feature, prepare to push it from your local git repo to Github.

Stage all of your changes with the `git add .` command. This sort of takes a screenshot of your current changes that git will keep track of.

If you only want to stage specific files instead of everything, you can replace the "`.`" With the names of the files you wish to stage.

## Commit changes

Make a commit of your changes using the `git commit -m “`_`commit_message`_`”`

Give a brief description of your changes in the commit message.

## Push changes

Push your changes to Github using the `git push -u origin` _`branch_name`_ command.

You should just be able to use the `git push` command, but to be safe you should use the first command when you push your changes for the first time, and then you can use `git push`

You may get a 403 error that I got saying that your permission is denied. What fixed this for me was clearing my git credentials. To do this search up “Credential Manager” in your search bar, click on “Windows Credentials”, scroll down to your git/github credentials and remove them.

Try the command again. It should prompt you to log in to Github again.

## Create Pull Request

Check Github and you should see a neat popup prompting you to create a pull request. If not, manually go to the “Pull requests” tab.

Create a pull request to merge your branch into the main branch.

Add an appropriate comment for the pull request and create it.

Allow the other teammates to review your changes if necessary and when ready, merge the changes into the main branch.

## After changes are merged

Delete your now merged branch from the Github repo.

In your terminal, switch back to the main branch and use the `git pull` command to pull the merged changes from the main branch in Github to your local main branch.

Delete your local merged branch with `git branch -d` _`branch_name`_

Rinse and repeat from the "Create your own branch" step.
