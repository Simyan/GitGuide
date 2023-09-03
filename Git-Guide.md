## Git Basic Commands


> 1. &emsp; `git init` <br>  &emsp;&emsp; Initializes a new Git repository in the current working directory.<br>
> 1. &emsp; `git clone <repo>` <br>  &emsp;&emsp; Creates a copy of the specified remote repoistory in the working directory. By default it copies all of the version history as well. <br> &emsp;&emsp; It is possible to partially copy the contents by providing additional paramters, however this is not very common.<br>
> 2. &emsp; `git fetch` <br> &emsp;&emsp; Gets the latest missing changes from the remote to the local repository. <br> &emsp;&emsp; This will not reflect in your working directory.<br>
> 3. &emsp; `git merge <branch | commit>` <br>  &emsp;&emsp;  Gets the changes from the specified target into where the Head is currently pointing. This creates a new commit with <br> &emsp;&emsp; both the changes.<br>
> 4. &emsp; `git push` <br>  &emsp;&emsp; This pushes the new changes commited in your local repository to the remote repository.<br> 
> 5. &emsp; `git pull` <br>  &emsp;&emsp; This does the job of fetch and merge in one command. Normally we would use this to get changes from the remote repository.<br>
> 6. &emsp; `git checkout <branch | commit>` <br>  &emsp;&emsp; Changes the head to the specified target
> 6. &emsp; `git branch` <br>  &emsp;&emsp; List all of the branches.<br>
> 6. &emsp; `git branch <name>` <br>  &emsp;&emsp; Creates a new branch where the head is currently pointing.<br>
> 6. &emsp; `git checkout -b <name>` <br>  &emsp;&emsp; Creates a new branch where the head is currently point and also checks out the new branch.<br>




## Git Advanced Commands

> 11. &emsp; `git rebase` <br>  &emsp;&emsp; Bring in changes to specified target from source. This copies the commits from the source and appends it to the target. <br> &emsp;&emsp; This allows you to keep a clean history of commits as they will be linear. 
> 11. &emsp; `git rebase -i` <br>  &emsp;&emsp; This allows you to similarly copy commits onto target from source but additionally it also lets you perform various actions <br> &emsp;&emsp; to the range of commits that are being copied. You can reorder the commits, squash them into one, edit commits or even omit <br> &emsp;&emsp; them.   
> 11. &emsp; `git cherrypick <[commit ids]>` <br>  &emsp;&emsp; Let's you copy specified commits onto where the head is currently pointing.  
> 11. &emsp; `git reset` <br>  &emsp;&emsp; This allows you to rollback to your previous commits, you can specify how far back you want to go relative to the HEAD. <br> &emsp;&emsp;  Useful for rolling back file changes in staging area or commits in your local repository  
> 11. &emsp; `git revert` <br>  &emsp;&emsp; This will rollback your changes similarly except it will append it as a new commit. <br> &emsp;&emsp; Useful for rolling back changes that have already been pushed to remote.
> 11. &emsp; `git branch -f <name>` <br>  &emsp;&emsp; Moves the specified branch to where the head is currently pointing. Use this wisely.

## Additional Information

&emsp; This section will introduce you to some aditional resouces that will help you get a better understanding of various concepts of Git and how to <br> &emsp; approach certain scenarios

> ### **Understanding the basics**
> [This article](https://agripongit.vincenttunru.com/) is an excellent introduction to the basic workflow of git. 

> ### **Interactive tutorials**
> [I highly recommend this website](https://learngitbranching.js.org/). It is an interactive guide where you will be asked to complete levels by running git commands to complete the scenario. <br><br>  Below is a list of few important levels that will help you understand the following concepts. The website allows you to navigate directly to a given level of your choice from the level selector, the level column in the table will help you navigate it
>| Concept | Path to Level | 
>| ----------- | ----------- |
>| Rebase |  Main &rarr; Introduction Sequence &rarr; 4️⃣
>| HEAD |  Main &rarr; Ramping Up &rarr; 1️⃣
>| Relative Refs (~) |  Main &rarr; Ramping Up &rarr; 3️⃣
>| Interactive Rebase |  Main &rarr; Moving Work Around &rarr; 2️⃣
>| Cherry picking |  Main &rarr; Moving Work Around &rarr; 1️⃣





> ### **Rebasing**
> [This article](https://www.atlassian.com/git/tutorials/merging-vs-rebasing) will provide some key points on how to use rebase responsibly and in which senarios can they be helpful.

>### **Reset vs Checkout vs Revert**
>| Command | Scope | Common Use Case |
>| ----------- | ----------- | ----------- |
>| git reset | Commit Level | Discard commits in a private branch or throw away uncommited changes 
>| git reset | File level | Unstage a file 
>| git checkout | Commit level | Switch between branches or inspect old snapshots 
>| git checkout | File level | Discard changes in the working directory
>| git revert | Commit level | Undo commits in a public branch
>| git revert | File level | N/A

