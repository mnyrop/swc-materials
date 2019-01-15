# Contents
- [Setup](#setup)
- [Version Control with Git](#version-control-with-git)
  + [Automated Version Control](#automated-version-control)
  + [Creating a Repository](#creating-a-repository)
  + [Tracking Changes](#tracking-changes)
  + [Ignoring Things](#ignoring-things)
  + [Remotes in GitHub](#remotes-in-github)
  + [Collaborating](#collaborating)
  + [Conflicts](#conflicts)
  + [Open Science](#open-science)
  + [Licensing](#licensing)
  + [Citation](#citation)
  + [Hosting](#hosting)
  + [Exploring History](#exploring-history-at-the-end-if-theres-time)

# Setup

__Setup check in:__

- [ ] Do you have the necessary software (Bash, Git, and Python) installed?
- [ ] Do you have [Jupyter notebooks](https://jupyter.org/install) installed? (You can check by opening a Terminal and entering the command `jupyter notebook`. This should open a browser.)
- [ ] Do you have the demo data for [bash](http://swcarpentry.github.io/shell-novice/setup.html) and [python](https://swcarpentry.github.io/python-novice-inflammation/setup/) downloaded?
- [ ] Do you have a [GitHub account](https://github.com/join)?
- [ ] Do you have 2 color post-its?





# Version Control with Git


## Automated Version Control


#### Questions:
- What is version control and why should I use it?

#### Notes:
- Version control – keeps track of changes and allows for greater control over them
- Manages collaboration and change conflicts


## Setting Up Git


#### Questions:
- How do I get set up to use Git?

#### Notes:
- Git is the software, GitHub is a popular *service* for hosting content that is version controlled by Git
- Your local Git needs to be configured to work with your GitHub account

#### Activity:
- [ ] Configure Git to use your user name with `git config --global user.name "your-username"`
- [ ] Configure Git to use your email with `git config --global user.email "your@email.address"`
- [ ] Configure your Git to use Nano as its text editor with `git config --global core.editor "nano -w"`
- [ ] Check your Git configuration with `git config --list`
- [ ] Check possible config commands with `git config -h`


## Creating a Repository


#### Questions:
- Where does Git store information?

#### Notes:
- A repository is where your Git project files and the history of all your project’s commits live
- `git init` initializes a repository (and everything in it!)
- `git status` shows the repository's current status
- The Git repository history and info lives in a directory called `.git`

#### Activity:

- [ ] `cd ~/Desktop`
- [ ] `mkdir planets`
- [ ] `cd planets`
- [ ] `git init` initializes the `planets` repository


## Tracking Changes

#### Questions:
- How do I record changes in Git?
- How do I check the status of my version control repository?
- How do I record notes about what changes I made and why?

#### Notes:
- Adding and committing
- Commit messages
- Reading the commit history

#### Activity:

- [ ] Check current directory with `pwd`
- [ ] Make sure you are in `~/Desktop/planets` using `cd`
- [ ] Use Nano to make a file `nano mars.txt` and add the sentence 'Cold and dry, but everything is my favorite color' to it before saving
- [ ] Use `ls` to list the directory contents
- [ ] Use `cat mars.txt` to print out the file's content
- [ ] Try `git status` again
- [ ] Tell Git to track our new file with `git add mars.txt`
- [ ] Try `git status` again
- [ ] Commit the changes and give a message about what the changes are with `git commit -m 'start notes on mars as a base'`
- [ ] Try `git status` again
- [ ] Look at the commit history with `git log`
- [ ] Add some additonal info to `mars.txt` with `nano mars.txt`, for example 'The two moons may be a problem for Wolfman'
- [ ] Try `git status` again
- [ ] Try `git diff`
- [ ] Try committing the new changes with `git commit -m 'add concerns about the moons and wolfman'`
- [ ] Try `git status` again
- [ ] Add the file with `git add mars.txt` then retry the commit `git commit -m 'add concerns about the moons and wolfman'`
- [ ] Add a third piece of info to the file with `nano mars.txt`, e.g., 'The mummy will appreciate the lack of humidity'
- [ ] Print it with `cat mars.txt`
- [ ] Try `git diff`
- [ ] Add the file with `git add mars.txt`
- [ ] Commit the changes with `git commit -m 'add mummy climate concerns'`
- [ ] Try `git status` again
- [ ] Look at the commit history with `git log`
- [ ] Try `git log -1`. What happens?
- [ ] Try `git log --oneline`
- [ ] Try `git log --oneline --all --decorate`




## Ignoring Things

#### Questions:
- How can I tell Git to ignore files I don’t want to track?

#### Notes:
- There will often be files you don't want Git to track, for security or efficiency reasons
- Ignored files, directory, and file patterns are listed in a `.gitignore` file

#### Activity:
- [ ] Make sure we're still in `~/Desktop/planets` with `pwd`
- [ ] Make a new directory with `mkdir results`
- [ ] Add a few files with `touch a.dat b.dat results/a.out results/b.out`
- [ ] Run `git status`
- [ ] Make a `.gitignore` file with `nano .gitignore` with `*.dat` on the first line and `results/` on the second line.
- [ ] Print out the file's content with `cat .gitignore`
- [ ] Run `git status` again
- [ ] Add and commit the `.gitignore` file with `git add .gitignore` and `git commit -m 'ignore data files and results folder'`
- [ ] Run `git status again`
- [ ] Try running `git add a.dat`. What happens?
- [ ] Run `git status --ignored`

## Remotes in GitHub

#### Questions:
- How do I share my changes with others on the web?

#### Notes:
- Repository remotes (origin)
- Git Push
- Git Pull

#### Activity:
- [ ] Log into [GitHub](https://github.com)
- [ ] Add a new public repository called 'planets'
- [ ] Copy the 'quick setup' link (it should be 'https://github.com/YOUR_USERNAME/planets.git')
- [ ] And paste it into your terminal for the command `git remote add origin 'https://github.com/YOUR_USERNAME/planets.git'`
- [ ] Run `git remote -V`
- [ ] Run `git push -u origin master` and enter your GitHub password when prompted
- [ ] Try `git pull origin master`
- [ ] Refresh your repository page on GitHub. What do you see?

## Collaborating

#### Notes:
- Collaborator permissions
- Git clone

#### Questions:
- How can I use version control to collaborate with other people?

#### Activity:
- [ ] Pair up with a neighbor and decide who will start as the 'owner' and who will start as the 'collaborator'
- [ ] __Owner:__ click on the 'Settings' tab on your `planets` repository in GitHub, navigate to 'Collaborators' and add your partner's GitHub username.
- [ ] __Collaborator:__ Go to <https://github.com.notifications> and accept the owner's request to collaborate on their repository
- [ ] __Collaborator:__ clone the owner's `planets` repository onto your computer as `OWNER_USERNAME-planets` with `git clone 'https://github.com/OWNER_USERNAME/planets.git' ~/Desktop/OWNER_USERNAME-planets`
- [ ] __Collaborator:__ Change directory into the newly cloned repository with `cd`
- [ ] __Collaborator:__ Add a new file `nano pluto.txt` with the content 'It is so a planet!'
- [ ] __Collaborator:__ Run `cat pluto.txt`
- [ ] __Collaborator:__ Add the file with `git add pluto.txt`
- [ ] __Collaborator:__ Commit the changes and add a commit message `git commit -m 'add notes about Pluto'`
- [ ] __Collaborator:__ Push the changes to the owner's remote repository on GitHub with `git push origin master`
- [ ] __Owner:__ Refresh the repository page on GitHub
- [ ] __Owner:__ Back in the bash terminal, make sure you are in `planets` with `pwd` and `cd` if necessary
- [ ] __Owner:__ Pull in the new changes from the remote repository on GitHub with `git pull origin master`
- [ ] __Owner and Collaborator:__ switch roles and add another planet



## Conflicts

#### Questions:
- What do I do when my changes conflict with someone else’s?

#### Notes:
- When working on the same files, collaborators can create content conflicts.
- Version control with Git provides means for managing and reconciling conflicts
- Use `git fetch` and `git pull` often to avoid/preempt conflicts

#### Activity:
- [ ] __Collaborator:__ Create a conflict by adding another line to `mars.txt` with `nano`: "This is a new line in OWNER_USERNAME's copy"
- [ ] __Collaborator:__ Push the change to GitHub with `git add mars.txt`, `git commit -m 'add a line to OWNER_USERNAME copy'`, and `git push origin master`
- [ ] __Owner:__ Make a change in your own copy of `mars.txt` with `nano`: 'this is a different line added'
- [ ] __Owner:__ Push the change to GitHub with `git add mars.txt`, `git commit -m 'add a line in my copy'`, and `git push origin master`. What happens?
- [ ] __Owner:__ Pull in collaborator's changes with `git pull origin master`
- [ ] __Owner:__ Look at the conflict with `cat mars.txt`
- [ ] __Owner:__ Use `nano mars.txt` to reconcile the conflict.
- [ ] __Owner:__ Merge the changes by committing them with `git add mars.txt`, `git status`, `git commit -m 'merge in changes from GitHub'`, and finally `git push origin master`
- [ ] __Collaborator:__ Pull in the newly reconciled change with `git fetch` and `git pull origin master`
- [ ] __Collaborator:__ Check the results with `cat mars.txt`


## Open Science

#### Questions:
- How can version control help me make my work more open?




## Licensing

#### Questions:
- What licensing information should I include with my work?




## Citation

#### Questions:
- How can I make my work easier to cite?




## Hosting

#### Questions:
- Where should I host my version control repositories?


## Exploring History (at the end, if there's time)

#### Questions:
- How can I identify old versions of files?
- How do I review my changes?
- How can I recover old versions of files?


> __Full Tutorial:__ <https://swcarpentry.github.io/git-novice/>

