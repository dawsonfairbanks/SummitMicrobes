# Summit Microbes
This is a working data repository for the 2019 NEON Science Summit Soil Micro/Biogeochemistry Working Group

## Working in this repository

1. Clone the master repository to your desktop.
2. Create a branch from the master repository
3. Make and push changes when you're ready to submit your changes- stage and commit your changes and push to the repository.


# Introduction to Version Control with Git ##
this link below is a helpful guide
[https://guides.github.com/activities/hello-world/](https://guides.github.com/activities/hello-world/)

## first fork the repository to your github account
### fork = copy repository on github
### clone = copy to local machine

## copy to your local machine by moving to the directory you would like to clone to
```

cd ~/Documents #moves to documents from your home directory
mkdir DirectoryName #make a directory to add your github clone
cd DirectoryName #move to directory you would like to clone to
```


## clone respository from the master repository
```
git clone https://github.com/NEONScience/SummitMicrobes.git
git config --global user.name "<githubusername>" #you may not need these lines if you have used git recently
git config --global user.email <githubemail>
git init . #initialize current wd
```

# Branch from the master repository
## Create a new branch from the master repository
```
git checkout -b branchNameHere
```
## To switch branches

```
git checkout branchNameHere
git checkout master
```

## Check what branch you are in
```
git branch
```
# Make changes to your working branch
```
mkdir example_directory #create new folder
cd example_directory #move into that folder
nano sometextfile.txt #create new file using nano text editor
ls #use ls command to view it
git branch #since the file is new, it is ony in your branch, shows you what branch you are in
#can check master branch using above commands using git checkout to move branches and git status to view changes
```

# Move back into working branch and stage and commit new file
```
git add sometextfile.txt
git status
git commit -m 'added some text file' #include some useful comment about what has been changed since last commit

```
At this point you have taken a snapshot of changes to the branch, and there are likely more changes and work to be done. Make commits along the way at logical points <br>
Think of each commit as a consecutive stage, commit messages capture this history of your changes. <br>
Next, it is time to merge code between branches. <br>
Do this when you are finished working, don't wait too long to avoid merge conflicts. <br>

#### If you made changes in the master branch, you can easily revert with git revert or git reset to undo any undesired changes
```
#in master branch
git revert 
git reset

#can revert by individual files. e.g. if I made the sometextfile.txt file in the master branch I could revert with git checkout:
git checkout sometextfile.txt
```

#### Now, we have successfully made our changes in our newly created branch and next we need to merge..
# Merge code between branches
## Move to the master branch to merge your newly created branch
```
git checkout master # move to master branch
git status # check status, you will see the original file you had cloned with no changes
git merge branchNameHere # merge your branch

```

# Getting back to GitHub- git push
Everything to this point is still on your local machine, use git push to push to GitHub
```
git push

```

# A final note..
We have successfully merged our branch to the master branch. You can delete that branch you've created:
```
git branch -d branchNameHere

```

# Think: Add --> Commit --> Push Data
add is the staging command for git. *want to use add the most when working with git* <br>
want to add, but not ready to commit <br>
adding means you can still can work on it <br>
commit is where you get to unique id (think of a save history) <br>
commit is focal point of version control, where info is being stored forever <br>
with IDs can go back in time to the old versions you have made <br>
merging syncs your branch to the master branch <br>
push uploads them to github <br>

