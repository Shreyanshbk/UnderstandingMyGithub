# 1. Git Workflow

Git helps in version control by allowing you to keep a track of changes you made to the project over time. Git records and stores the changes you made to a project. 

## git init
This command helps to make any directory a git directory. 'init' stands for initialize and tells git tp start tracking the changes in the project. The project is now turned into a git project.

## Three Crucial Parts of a Git Project

### Working Directory
This is directory where you do all the changes, addition and deletion. 

### Staging Area
Lists all the changes made to the working directory. The changes to the project are first brought to the staging area before commit. 

### Repository
Repositories are Git's permanent storage for changes as different version of the project. 

## git status
The project is changed in the working directory. In order to check the status of those changes 'git status' command is used. 

## git add <filename/s>
Inorder to commit any changes to the repository, the changes need to be brought from the working directory to the staging area so that the git starts tracking it. "git add filename" does the job for us. git add can take more than one file space separated.

## git diff <filename> 
This command compares the file in the working directory and the staging area and lists the additions and the deletions made to the file. 

## git commit -m "Complete the text"
git commit saves changes permanently to the repositories with the message in the inverts. The message generally should be in present tense.

## git log
In order to check the history of commits "git log" command is used.

# 2. Backtracking In Git

## git show HEAD
Head commit is the commit on which you currently are (most recent commit most of the time.). 

## git checkout HEAD <filename>
You probably made some changes in the working directory and didn't like. This command will make the directory as before. 

## git reset HEAD <filename>
This commands helps to unstage a file. The contents in the stage become similar to HEAD. However, the working directory remains unaffected. 

## git reset <SHA>
The first seven characters of the commit SHA takes the git to the version of project that existed that time. 

# 3. Branching in Git
## git branch
This commands helps to find out the current branch on which you are working.

## git branch <new_branch_name>
This command creates a new branch with the above name. 

## git checkout <branch_name>
This command takes us to a particular branch. 

## git merge <branch_name>
Merges the branch with the master. You must be in the master. 

## Resolving merge conflicts
Merge conflicts occurs when a branch try to merge to a master which has commited the same text after the branch was made. In this situation git marks all the texts to labels of HEAD and branch_name. Remove whichever you don't want along with git sepcial symbols and commit. 

## git branch -d <branch_name>
This command is used to delete the branch given above. 

# 4. Team Projects in Git

## Remotes
Git helps collaborative work on remotes which is a shared Git allowing users to work from their location. Team meambers work independently and update projects as they feel like. 

## git clone <remote_location> <clone_name>
Helps to clone the repository on the remote_location with the clone_name on the local machine. 

## git remote -v
Displays the list of Git Projects remotes. Git automatically names the remote repository to 'origin'.

## git fetch 
This command is used to fetch any change made on the remote directory. These changes are not reflected in the local repository. It brings the changes to 'remote branch' (origin/master). which are then merged with the master branch using "git merge origin/master".

## git push origin <optional_branch_name>
This command pushes the local changes to the original repository. 

# 5. The Workflow

Collaborating on github is usually done in the following way: 
1. Collaborator clones/fetches(and merges) the remote repository and with the local master before changing or adding any new feature. 
2. Create a new branch to work on. 
3. Develop the new feature and commit it on the branch. 
4. Fetch and merge for any changes while you were working on the feature.
5. Push the branch onto the main repository for the owner to see and merge with master. 





