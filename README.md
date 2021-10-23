# Basic Git commands

<table>
  <tr>
    <th> Git task
    <th> Notes 
    <th> Git commands 
  </tr>
  <tr>
    <td> Tell Git who you are 
    <td width="320px"> Configure the author name and email address to be used with your commits.
Note that Git strips some characters (for example trailing periods) from user.name. 
    <td width="400px"> git config --global user.name "Sam Smith" <br>
git config --global user.email sam@example.com 
  </tr>
  <tr>
    <td> Create a new local repository 
    <td>   
    <td> git init 
  </tr>
  <tr>
    <td> Check out a repository 
    <td> Create a working copy of a local repository: 
    <td> git clone /path/to/repository 
  </tr>
  <tr>
    <td> 
    <td> For a remote server, use:
    <td> git clone username@host:/path/to/repository
  </tr>
  <tr>
    <td> Add files
    <td> Add one or more files to staging (index):
    <td> git add <filename> <br> git add *
  </tr>
  <tr>
    <td> Commit
    <td> Commit changes to head (but not yet to the remote repository):
    <td> git commit -m "Commit message"
  </tr>
  <tr>
    <td> 
    <td> Commit any files you've added with git add, and also commit any files you've changed since then:
    <td> git commit -a
  </tr>
  <tr>
    <td> Push
    <td> Send changes to the master branch of your remote repository:  
    <td> git push origin master
  </tr>
  <tr>
    <td> Status
    <td> List the files you've changed and those you still need to add or commit:  
    <td> git status
  </tr>
  <tr>
    <td> Connect to a remote repository
    <td> If you haven't connected your local repository to a remote server, add the server to be able to push to it:  
    <td> git remote add origin <server> 
  </tr>
  <tr>
    <td> 
    <td> List all currently configured remote repositories:  
    <td> git remote -v
  </tr>
  <tr>
    <td> **Branches**
    <td> Create a new branch and switch to it:  
    <td> git checkout -b <branchname>
  </tr>
  <tr>
    <td> 
    <td> Switch from one branch to another:  
    <td> git checkout <branchname>
  </tr>
  <tr>
    <td> 
    <td> List all the branches in your repo, and also tell you what branch you're currently in:  
    <td> git branch
  </tr>
  <tr>
    <td> 
    <td> Delete the feature branch:  
    <td> git branch -d <branchname>
  </tr>
  <tr>
    <td> 
    <td> Push the branch to your remote repository, so others can use it:  
    <td> git push origin <branchname>
  </tr>
  <tr>
    <td> 
    <td> Push all branches to your remote repository:  
    <td> git push --all origin
  </tr>
  <tr>
    <td> 
    <td> Delete a branch on your remote repository:  
    <td> git push origin :<branchname>
  </tr>
  <tr>
    <td> 
    <td> To list remote branches: 
    <td> git branch -r
  </tr>      
  <tr>
    <td> ***Update from the remote repository***
    <td> Fetch and merge changes on the remote server to your working directory:  
    <td> git pull
  </tr>
  <tr>
    <td> 
    <td> To merge a different branch into your active branch:  
    <td> git merge <branchname>
  </tr>
  <tr>
    <td> 
    <td> View all the merge conflicts: <br> View the conflicts against the base file: <br> Preview changes, before merging:
    <td> git diff  <br> git diff --base <filename> <br> git diff <sourcebranch> <targetbranch>
  </tr>
  <tr>
    <td> 
    <td> After you have manually resolved any conflicts, you mark the changed file: 
    <td> git add <filename>
  </tr>
  <tr>
    <td> ***Tags***
    <td> You can use tagging to mark a significant changeset, such as a release:  
    <td> git tag 1.0.0 <commitID>
  </tr> 
  <tr>
    <td> 
    <td> CommitId is the leading characters of the changeset ID, up to 10, but must be unique. Get the ID using:
    <td> git log
  </tr>
  <tr>
    <td> 
    <td> Push all tags to remote repository:  
    <td> git push --tags origin 
  </tr>
  <tr>
    <td> ***Undo local changes***
    <td> If you mess up, you can replace the changes in your working tree with the last content in head:
Changes already added to the index, as well as new files, will be kept.  
    <td> git checkout -- <filename>
  </tr>
  <tr>
    <td> 
    <td> Instead, to drop all your local changes and commits, fetch the latest history from the server and point your local master branch at it, do this:   
    <td> git fetch origin <br> git reset --hard origin/master
  </tr>
  <tr>
    <td> Search	
    <td> Search the working directory for foo():  
    <td> git grep "foo()"
  </tr> 
</table>

