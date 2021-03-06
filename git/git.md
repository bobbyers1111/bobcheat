***
# git cheatsheet
***
### General Workflow..

1. Fetch and merge changes from the remote
2. Create a branch to work on a new project feature
3. Develop the feature on your branch and commit your work
4. Fetch and merge from the remote again (in case new commits were made while you were working)
5. Push your branch up to the remote for review

***
### Git Terminology

- A *clone* is a local copy of a remote repository

- *origin* is an alias for the remote repository's URL

- Everything needed to access the remote is in the .git/config file. Example..

>    [core]  
>>	    bare = false  
>>	    repositoryformatversion = 0  
>>	    filemode = true  
>>	    logallrefupdates = true  

>    [remote "origin"]  
>>	    url = https://github.com/bobbyers1111/bobcheat.git  
>>	    fetch = +refs/heads/*:refs/remotes/origin/*  

>    [branch "master"]  
>>	    remote = origin  
>>	    merge = refs/heads/master  

***
<<<<<<< Updated upstream
### Git Objects

>Stored in the *Object Store* and consists of the following objects..

1. **Commit Object**
    1. Is a small text file
    1. Is all git needs to rebuild the full contents of a commit
    1. Stores the following information..
        1. Commit user information
        1. Commit message
        1. Reference to the commit's parent(s)
        1. Reference to the root tree of the project

2. **Annotated tag**
> Is a reference to a specific commit

3. **Tree**
> List of directories and files inside a project

4. **Blob**
> Contents of a any file being managed by git

***
### Git IDs

* A git ID is the name of a git object

* Stored as a 40-char hex string

* Often displayed as only the first 7 characters

* You may use the first few ID chars (min 4) in git so long as it is unique within the repository

* Uses SHA1 algorithm

* Can manually compute a SHA1 for a file with..

>git hash-object *file*

***
### Commands Overview..
=======
### remote, local, etc.
- Two fundamental starting scenarios..
- - Already have a local repository => add the remote
>(the add command also sets up an alias for the remote; e.g., 'origin')  
>>git remote add origin https://github.com/bobbyers1111/reposC.git  
>>git push -u origin master  
>>
- - Already have a remote repository => clone the remote
>>git clone https://bitbucket.org/atlassian_tutorial/helloworld.git  
>>
>>>>>>> Stashed changes

<<<<<<< Updated upstream
#### git help *gitcmd*
>Displays in-depth help

#### git *gitcmd* -h
>Displays command line syntax only

#### git add
>Stages files from the working directory to the staging area

#### git branch
>Displays the branch upon which you're currently working

#### git branch branchname
>Creates a new branch

#### git branch -d branchname
>Deletes an old branch

#### git checkout branchname
>Changes current working branch to branchname

#### git checkout HEAD
>Will OVERWRITE any changes to the local file and retrieve the most recent committed version from the repository.

#### git clone remote local
>Makes a local copy of a remote branch
=======
- A *clone* is a local copy of a remote repository

- *origin* is an alias for the remote repository's URL

- Everything needed to access the remote is in the .git/config file. Example..


>    [core]  
>>	    bare = false  
>>	    repositoryformatversion = 0  
>>	    filemode = true  
>>	    logallrefupdates = true  

>    [remote "origin"]  
>>	    url = https://github.com/bobbyers1111/bobcheat.git  
>>	    fetch = +refs/heads/*:refs/remotes/origin/*  
>>>>>>> Stashed changes

>    [branch "master"]  
>>	    remote = origin  
>>	    merge = refs/heads/master  

<<<<<<< Updated upstream
#### git config
>Get and set repository or global options.

>>--system: apply command to every repository for every user on current system.

>>--global: applies to every repository for the current user on current system.

>>--local: applies only to the current repository (highest precedence).


#### git config core.editor <editor>
>Set editor for git operations requiring an editor

#### git diff
>Shows the difference between the working directory and the staging area

#### git fetch
>Retrieve any changes that may have been made to the clone's origin. Changed files are placed in a REMOTE BRANCH.

#### git init
> Creates a new Git repository

#### git log
>Shows a list of all previous commits

#### git merge branchname
>Merges changes from branchname into the current working branch.

#### git push [-u] remote localbr
>Pushes your local changes to the branch specified by *remote*  
>*remote* can be either an alias (e.g., *origin*) or a full URL  
>Use '-u' to enable tracking so git will warn you of out-of-sync files  

#### get remote -v
>Lists the known remotes of the files in the current working repository. Each file listed at least twice - once as a fetch, the other as a push.
=======
***
#### Create a new repository from command line

    echo "# reposC" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin https://github.com/bobbyers1111/reposC.git
    git push -u origin master

    …or push an existing repository from the command line

    git remote add origin https://github.com/bobbyers1111/reposC.git
    git push -u origin master
>>>>>>> Stashed changes

***
### Commands Overview..

#### git help *gitcmd*
>Displays in-depth help

#### git *gitcmd* -h
>Displays command line syntax only

#### git add
>Stages files from the working directory to the staging area

<<<<<<< Updated upstream
#### git show HEAD
>Display everything the git log command displays for the HEAD commit, plus all the file changes that were committed.

#### git status
>Inspects the contents of the working directory and staging area

***
#### Create a *new* repository from command line..

>    echo "# reposC" >> README.md
=======
#### git branch
>Displays the branch upon which you're currently working

#### git branch branchname
>Creates a new branch

#### git branch -d branchname
>Deletes an old branch

#### git checkout branchname
>Changes current working branch to branchname

#### git checkout HEAD
>Will OVERWRITE any changes to the local file and retrieve the most recent committed version from the repository.

#### git clone remote local
>Makes a local copy of a remote branch

#### git commit
>Permanently stores file changes from the staging area in the repository
>>>>>>> Stashed changes

>    git init

>    git add README.md

>    git commit -m "first commit"

>    git remote add origin https://github.com/bobbyers1111/reposC.git

<<<<<<< Updated upstream
>    git push -u origin master

#### Push an *existing* repository from the command line..

>    git remote add origin https://github.com/bobbyers1111/reposC.git

>    git push -u origin master
=======
#### git config core.editor <editor>
>Set editor for git operations requiring an editor

#### git diff
>Shows the difference between the working directory and the staging area

#### git fetch
>Retrieve any changes that may have been made to the clone's origin. Changed files are placed in a REMOTE BRANCH.

#### git init
> Creates a new Git repository

#### git log
>Shows a list of all previous commits

#### git merge branchname
>Merges changes from branchname into the current working branch.

#### git push [-u] remote localbr
>Pushes your local changes to the branch specified by *remote*  
>*remote* can be either an alias (e.g., *origin*) or a full URL  
>Use '-u' to enable tracking so git will warn you of out-of-sync files  

#### get remote -v
>Lists the known remotes of the files in the current working repository. Each file listed at least twice - once as a fetch, the other as a push.

#### git reset HEAD filename
>This command resets the file in the staging area to be the same as the HEAD commit. It does not discard file changes from the working directory, it just removes them from the staging area.

#### git reset SHA
>Resets to a previous commit identified by the first 7 digits of its SHA from 'git log'. Conceptually..

              Before reset..
              [A] ------ [B] ------ [C] ------ [D] ------ [HEAD]
              
              After reset..
              [A] ------ [B] ------ [HEAD]

#### git show HEAD
>Display everything the git log command displays for the HEAD commit, plus all the file changes that were committed.

#### git status
>Inspects the contents of the working directory and staging area
>>>>>>> Stashed changes
