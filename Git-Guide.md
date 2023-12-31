## Git Basic Commands


`git init` <br>   Initializes a new Git repository in the current working directory.<br><br>
`git clone <repo>` <br> Creates a copy of the specified remote repoistory in the working directory. By default it copies all of the version history as well. It is possible to partially copy the contents by providing additional paramters, however this is not very common.<br><br>
`git fetch` <br> Gets the latest missing changes from the remote to the local repository. This will not reflect in your working directory.<br><br>
`git merge <branch | commit>` <br> Gets the changes from the specified target into where the Head is currently pointing. This creates a new commit with both the changes.<br><br>
`git push` <br> This pushes the new changes commited in your local repository to the remote repository.<br><br>
`git pull` <br> This does the job of fetch and merge in one command. Normally we would use this to get changes from the remote repository.<br><br>
`git checkout <branch | commit>` <br>  Changes the head to the specified target <br><br>
`git branch` <br>  List all of the branches.<br><br>
`git branch <name>` <br>   Creates a new branch where the head is currently pointing.<br><br>
`git checkout -b <name>` <br>   Creates a new branch where the head is currently point and also checks out the new branch.<br><br>




## Git Advanced Commands

`git rebase` <br>   Bring in changes to specified target from source. This copies the commits from the source and appends it to the target. This allows you to keep a clean history of commits as they will be linear.<br><br>
`git rebase -i` <br>   This allows you to similarly copy commits onto target from source but additionally it also lets you perform various actions to the range of commits that are being copied. You can reorder the commits, squash them into one, edit commits or even omit them.<br><br>
`git cherrypick <[commit ids]>` <br>   Let's you copy specified commits onto where the head is currently pointing.<br><br>
`git reset` <br>   This allows you to rollback to your previous commits, you can specify how far back you want to go relative to the HEAD. Useful for rolling back file changes in staging area or commits in your local repository.<br><br>
`git revert` <br>   This will rollback your changes similarly except it will append it as a new commit. Useful for rolling back changes that have already been pushed to remote.<br><br>
`git branch -f <name>` <br>   Moves the specified branch to where the head is currently pointing. Use this wisely.<br><br>

## Additional Information

 This section will introduce you to some aditional resouces that will help you get a better understanding of various concepts of Git and how to approach certain scenarios.

### **Understanding the basics**
[This article](https://agripongit.vincenttunru.com/) is an excellent introduction to the basic workflow of git. 

### **Interactive tutorials**
[I highly recommend this website](https://learngitbranching.js.org/). It is an interactive guide where you will be asked to complete levels by running git commands to complete the scenario. <br><br>  Below is a list of few important levels that will help you understand the following concepts. The column "Path to Level" will help you with navigating the level selector. 
| Concept | Path to Level | 
| ----------- | ----------- |
| Rebase |  Main &rarr; Introduction Sequence &rarr; 4️⃣
| HEAD |  Main &rarr; Ramping Up &rarr; 1️⃣
| Relative Refs (~) |  Main &rarr; Ramping Up &rarr; 3️⃣
| Interactive Rebase |  Main &rarr; Moving Work Around &rarr; 2️⃣
| Cherry picking |  Main &rarr; Moving Work Around &rarr; 1️⃣





### **Rebasing**
[This article](https://www.atlassian.com/git/tutorials/merging-vs-rebasing) will provide some key points on how to use rebase responsibly and in which senarios can they be helpful.

### **Reset vs Checkout vs Revert**
| Command | Scope | Common Use Case |
| ----------- | ----------- | ----------- |
| git reset | Commit Level | Discard commits in a private branch or throw away uncommited changes 
| git reset | File level | Unstage a file 
| git checkout | Commit level | Switch between branches or inspect old snapshots 
| git checkout | File level | Discard changes in the working directory
| git revert | Commit level | Undo commits in a public branch
| git revert | File level | N/A

