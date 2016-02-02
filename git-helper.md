# 10 Steps to GitHub!  :octocat:
Okay, maybe it won't be exactly like this depending on if you use branches for features and how you name your Git repositories.  

For the most part, though, these are the basic 10 steps to creating your first local repo and connecting to a remote repository on GitHub.com!  

**Remember, after the first time through these steps and once you successfully have your local repository linked to your remote repository, start at Step 5 next time!**

#### Step One:
Create a folder for your project **inside** the directory of your choice.  You can do this using your Finder (Mac) or Windows Explorer.  Only use command line for things that require command line.

#### Step Two:
Open up Terminal (Mac) or your command line prompt with Git installed (Windows), and navigate to the project folder you just created using the ```cd``` command.  Once you're in the project folder, do:
```git
git init
```
  This creates your local Git repository in your project folder.  You can confirm this worked by entering ```ls -a```, and you should see a ```.git``` file in your project folder.

#### Step Three:
If you haven't already created your remote repository on GitHub.com, here's how:

* Open your browser and log into GitHub.com
* Create your remote Git repository by clicking on the **Repositories** tab from your profile page.  
* Once that tab is shown, click the **New** button.  
* Give your remote repository a meaningful name relevant to your project idea, a description, choose "public" for the repository type, and initialize it with a README.md file.  Create the repo.  
* Once the repository is created, copy the link for your repository
```Command + C``` (Mac)
```Control + C``` (Windows) 
or click the **Copy to Clipboard** button.

#### Step Four:
Switch back to your terminal.  On the command line, enter:
```git
git remote add origin <paste link here>
```
  You can verify this worked by typing 

```git
git remote -v
```
  and you should see that your local repository (named ```origin```) is linked to fetch from/push to your remote repository at the link you provided.

#### Step Five: (Remember, start here if you already completed Steps 1 - 4, and you've navigated to the right directory in your command line)
Pull from your remote repository to your local repository by entering:
```git
git pull origin master
```

#### Step Six:
Using Finder (Mac) or Windows Explorer (Windows), you can now navigate to your project folder, open your project files in your text editor of choice, and work on your project.  When you're done adding features or making changes, save your files within your text editor.

#### Step Seven:
Switch back to your terminal.  Confirm that you have modified files since you made your project changes by entering:
```git
git status
```
  You will see those files as modified, and they may be shown in red.

#### Step Eight:
Add your newly modified file(s) to the Git staging area by entering:
```git
git add <insert filename here>
```
  You can do this individually or add them all at once by entering:
```git
git add .
```
  You can confirm that staging files was successful by entering ```git status``` and you should see the files now staged.

#### Step Nine:
Commit your staged files by entering:
```git
git commit -a -m "Leave some commit message here"
```
  You can confirm that committing files was successful by entering ```git status``` and you should see the files now committed.

#### Step Ten:
Push your files to your remote repository on GitHub.com by entering:
```git
git push origin master
```
  Note: if your local repo is not named ```origin``` or you've been working on branches other than ```master```, that command won't work and you'll need to adjust accordingly.

### Login to GitHub, go into your repo, and you should see your files and/or new changes! :tada:
