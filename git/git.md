***
## git notes
***
### General Workflow..

1. Fetch and merge changes from the remote
2. Create a branch to work on a new project feature
3. Develop the feature on your branch and commit your work
4. Fetch and merge from the remote again (in case new commits were made while you were working)
5. Push your branch up to the remote for review
***
### Commands Overview..

#### git init
> Creates a new Git repository

#### git status
>>Inspects the contents of the working directory and staging area

#### git add
>>Stages files from the working directory to the staging area

#### git diff
>>Shows the difference between the working directory and the staging area

#### git commit
>>Permanently stores file changes from the staging area in the repository

#### git log
>>Shows a list of all previous commits

#### git show HEAD
>>Display everything the git log command displays for the HEAD commit, plus all the file changes that were committed.

#### git checkout HEAD
>>Will OVERWRITE any changes to the local file and retrieve the most recent committed version from the repository.

#### git checkout branchname
>>Changes current working branch to branchname

#### git reset HEAD filename
>>This command resets the file in the staging area to be the same as the HEAD commit. It does not discard file changes from the working directory, it just removes them from the staging area.

#### git reset SHA
>>Resets to a previous commit identified by the first 7 digits of its SHA from 'git log'. Conceptually..

              Before reset..
              [A] ------ [B] ------ [C] ------ [D] ------ [HEAD]
              
              After reset..
              [A] ------ [B] ------ [HEAD]

#### git branch
>>Displays the branch upon which you're currently working

#### git branch branchname
>>Creates a new branch

#### git branch -d branchname
>>Deletes an old branch

#### git merge branchname
>>Merges changes from branchname into the current working branch.

#### git clone remote local
>>Makes a local copy of a remote branch

#### get remote -v
>>Lists the known remotes of the files in the current working repository. Each file listed at least twice - once as a fetch, the other as a push.

#### git fetch
>>Retrieve any changes that may have been made to the clone's origin. Changed files are placed in a REMOTE BRANCH.

#### git push origin localbr
>>Pushes your local changes to the branch specified by 'origin'.
