
Lab: (Command Line) Push to a Remote Repository  

Note: This lab assumes that you have created a remote repository named projectb

In this lab, you will:
1. Clone your Bitbucket repository.
1. Create a commit in the local repository.
1. Push the commit to the remote repository.

***
1: Clone your Bitbucket repository.

1. Log into bitbucket.org.
1. Select the *projectb* repository.
1. Navigate to *projectb*. Click the plus sign on the left and select Clone this repository.
1. Copy the git clone command to your clipboard.
1. In a command line window, navigate to your repos directory.
1. Paste the git clone command that you copied. Execute the command. You have cloned an empty repository.
1. Change to the *projectb* directory using *cd projectb*.
1. View the contents of *projectb* using *ls -a*. You should see an empty working tree and a .git directory.
1. Execute *git remote -v*. You should see the URL to your remote repository, and see that the shortcut name of this remote repository is *origin*.

Congratulations, you have cloned your remote repository.

***
2: Create a commit in the local repository.

1. Execute *echo "# projectb's README" > README.md* in your projectb directory. This creates a README file in your working tree. This content will show on the home page for the repository on Bitbucket.
1. Execute *git add README.md* to add the README file to the staging area.
1. Execute *git commit -m "add README.md"* to commit to the local repository.

Congratulations, you have created a commit in the local repository.

***
3: Push the commit to the remote repository.

1. Execute *git push -u origin master*. The -u flag sets up the local and remote branches as tracking branches. *origin* is a shortcut name for the remote repository. *master* is the branch to push. We are pushing the default branch named master.
1. Execute *git status* and verify that your branch is up to date and there is nothing to commit.
1. In your browser, navigate to Bitbucket. Navigate to your *projectb* repository. Click on the Commits tab. You should see your commit. You have synchronized your local and remote repositories.
1. In Bitbucket, click on the Overview tab. You should see the content of the README.md file that you created.

Congratulations. You have cloned and committed to your remote repository.


