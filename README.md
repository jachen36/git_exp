# Objective
This project is test out and record a process where I can mimic a team working on a single project. 


## Resource

[Bitbucket GIT Tutorial](200~https://www.atlassian.com/git/tutorials/setting-up-a-repository)

## Common Situation 

- [x] Linear commits (a few commits with images to pretend to be working on an already started project)
- [ ] Download FORK to view repo's history or use git log
- [ ] Add change to previous commit (git commit --amend)
- [ ] made a small change but added file to the stage already
- [ ] git clone (show how to download repo)
- [x] Show what checkout does 
- [x] Make a lot of files and changes to many files. Found out you don't want to changes. do git checkout HEAD
- [ ] Someone make a change and git push and then pull (show how to get the latest version)
- [x] Look into a file and make some test changes. Save the file. Decide you don't want it. git checkout filename
- [ ] Make changes, commit, decided you want to remove that commit (git reset --soft HEAD)
- [ ] Create master, dev branch (describe their purpose, rebase for dev, merge with master)
- [ ] Multiple people create feature branch based on the dev branch
- [ ] Everybody submit their imcomplete branch to remote
- [ ] git pull to get everyone's remote branch and see them
- [ ] Make every commit 5 commits. Then rebase it because it is too messy
- [ ] One person do a PR and merge (make them constantly do git fetch and pull to get the latest show that it doesn't hurt and that you always is with the latest)
- [ ] Everyone update their repo and rebase to the latest dev
- [ ] Everyone submit their PR. Merge. (Show that your branch doesn't need to always be latest to merge)
- [ ] Merge dev to master to 'release' the project. (never directly rebase to master)[golden rule of rebase](https://www.atlassian.com/git/tutorials/merging-vs-rebasing#the-golden-rule-of-rebasing) "is anyone else looking at this branch? if yes, take yo
- [ ] Do merge vs rebase
- [ ] After opening a PR, the boss as you to rebase to the latest which requires git push --force-with-lease
- [ ] A merge conflict from rebasing with master which has a few features added. 
- [ ] A separate example that will be deleted later to show using merge vs rebase when trying to get the latest from master. 
- [ ] get a rebase error to see what happens.
- [ ] show how to use git stash (how to save changes temporary)
- [x] use git reset <file> when I don't want to add it anymore or git reset to unadd everything
- [ ] Figure out how to update all remote branch. Do you need to checkout each branch like master to do a git fetch?

## Instructions 

pre-work
* got to install git
* an agenda. There will be periodic breaks for people to catch up and to ask random questions and time to digest the information. 
* I am a visual person, so the beginning is using images to learn the basics commands

### Step 1: Create a bunch of logos 
Objects: 
	* git add -A -i = to show how to add and using interactive
	* git add, git commit = example on how this is used 
	* git checkout = show what this command does 
	* git status = show how to use
	* git log = see history 

Make multiple commits by changing the logo image in the new `misc` folder. By using image, it is much easier to see what happens with the different commit and when checkout is used. Interactive git helps to see what gets added because `logo.png` is hidden in `misc`. 

Direction:
1. Have everyone create their own local version first. 
	* `mkdir git_exp`
	* `cd git_exp`
	* `git init`
	* `mkdir misc && cd misc`
2. Create a logo.
	* `git status` = to show that git knows what files has been changed
	* `git add misc/logo.png`
		* explain working directory, staging, committed. working = rough draft, staging = things I want to submit, commiting = publish/finalizing
	* `git commit -m "Version 1 Logo"`
	* `git status` = do this again to show that you have a clean workstation
3. Repeat step 2 three times, but changing the original `logo.png` file.
4. See your change history
	* `git log --oneline` = show all the changes you have done
5. Checkout a commit
	* open the folder with the image because it updates when changing
	* ask people what people think will happen when you explain what that checkout is looking at a record in history
	* `git checkout <hash>` = to see a record in history and what it looked like then
	* explain the detach head state, if you make change just checkout again.
	* `git log --oneline --all` = without `--all` it will not display the future commits. make them figure that part out. how the hell do I get back to version 3. 
	* explain how to read the logs
	* `git status` = use often to see where you are at
6. Get back to latest commit
	* `git checkout master` = you cannot do `git checkout <hash same as master>` because you are just pointing to the same commit but not to master so it is still in detached head.  
7. Make changes to logo, create a new image and decide it isn't want you wanted anymore
	* `git status` = to show the changes
		* shows an edit file
		* shows an untracked file meaning it following this file. 
	* since this is wrong draft and you want to show it around. found out the boss hate it with a passion. boss like with curls and it more trendy than boxy. Ask what what are you suppose to do now? You overwrote the original. 
	* `git reset -h` = get some help. teach how to read it 
	* `git reset --hard` = be careful with anything that says hard or force. 
		* because the new file is untracked, it doesn't know what to do with it. 
		* delete the file
		* git status to show your work station is clean. 
	* `git checkout <any hash> && git checkout master` = go back to original state

Side things to explain
* `git commit -h` = to explain how to understand how to use the command and options

Notes 

```bash
$ git log --oneline
01543bf (HEAD -> master) Version 3 Logo
d7b9978 Version 2 Logo
512c0e4 Version 1 Logo
```


### Step 2: Review the commands but with github/remote





