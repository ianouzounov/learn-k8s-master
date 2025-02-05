# WELCOME!!!

### Now that you have forked a copy of the master repo, cloned the repo to your local machine, and have gotten started; let's go over the standard instructions that you will complete for each section where you will sync your local git repo with the remote repo and then create a branch for adding your own named folder to each section.  
###### (Part of this exercise helps reinforce the git workflows and gives practice reviewing and approving PRs and merging branches while also giving you a place to keep your class work stored remotely)

#### Step 1: Ensure your local version of the repo is up to date with origin/main
- use `git pull` to make sure your local main matches origin/main

#### Step 2: Create a local branch from main
- use `git checkout -b jrn-section-1` to create and edit a new branch (you can name it whatever you like; I used my intials in the example)

#### Step 3: Create a folder with your name in the section you are working on
- go to the section folder you are working on (section 1 in the example)
- use `mkdir <your_name>` to create your working folder for that section
- you will need to add a file so that the folder will be picked up in the git commit (empty folders are ignored)
- use `touch jrn_notes.md` or something similar to create a file
- you can then complete the work in the section and use your named subfolder to store all your work
- it is up to you when you want to do commits or create your pull request

#### Step 4: When ready - commit your changes to your local branch
- use `git add .` to stage all changes for commit (ensure you have actually saved your work; a big white dot next to the file name in VS code is a sign you haven't!)
- use `git commit -m "some_message_that_works"` to update your local branch
- rinse and repeat until you are ready to merge your changes with a pull request
- you can keep your branch locally or push to the remote version as below:
- use `git push -u origin <branch>` to push and track your local branch to the remote branch
- once that is done, any local changes can be pushed to remote with a simple `git push`

#### Step 5: When ready - submit a pull request to merge your branch with origin/main
- after your last commit; you will create a pull request
- this can be done via the [GH CLI](https://cli.github.com/) as shown below or in the GH UI if you have pushed your local branch to the remote branch
- (GH CLI) use `gh pr create -t "a title" -b "body statement"` to create a PR
- you may be prompted on where to create the PR; make sure you choose your remote fork of the repo
- Hint: if you are using the GH CLI, you can use `gh pr view --web` command to jump to the GH UI for the pull request

#### Step 6: Review the PR and approve the merge
- View your pull request in your forked repository on Github
- Hint: if you are using the GH CLI, you can use `gh pr view --web` command to jump to the GH UI for the pull request
- Make sure that all tests passed; review the changes to make sure they are what you expect
- Merge the pull request
- You will be prompted to delete the branch on your GH remote repo

#### Step 7: Cleanup and update your local branches
- Once the merge request is done; you can return to your local terminal and switch back to your main branch
- If you don't delete your local branch nothing evil will happen; but eventually you will notice that you have a ton of stale branches piling up (been there, done that lol) so to keep that from happening you can use `git branch -d <branch_name>` to tidy up the branch that remains after the PR
- Pull down the newly merged changes from your remote origin main branch by using the following command: `git pull`
