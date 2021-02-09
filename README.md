# What is Git?

Git is **free, open-source software distributed version control system**, commonly known as DVCS, that is designed to manage all the source code history.
For a developer it is beneficial tool, as it keep a history of commits, can reverse changes, and let developers to share their codes on a single platform.

# What is GitHub?

GitHub is a Web-based Hosting service for Git repositories with user-friendly GUI. In simple words we can say that, GitHub is a Online Web-based service that help to upload our repositoires online.
GitHub offers all the Gits' version control properties with additional features.
With GitHub, developers can easily work in groups, can share their repositories, access other developers' repositories, and store remote copies of repositories to serve as backup.
## What is the use of GitHub?
As we know what exactly GitHub is, let us now know a better understanding of its uses:
- ###### Easy Project Management
GitHub is a user-friendly Interface, where developers can coordinate, track, update their work.
- ###### Effective Team Management
GitHub Helps all the team members stay on same wavelength.
- ###### Easy Code Hosting
Through GitHub, all the codes and the documentation are located in one place. 
- ###### Increased Safety with Repositories
Repositories can be published privately, enclosed in the team. The repositaries can be used or reused by downloading(Cloning) them from GitHub.
- ###### Increase code Safety
GitHub uses tools to identify & analyze security vulnerabilities and coding errors. By using code scanning we can find, organize, and prioritize fixes for existing problems in our code. the popular tool used is CodeQl.
- ###### Improve Code Writing
By multiple team member working on same repository, help them to discuss any implementations, review the new code.



# What is Repository
Repository cointain all of our source code files, documentations, and other important files. Briefly a repository is a Project(comprised of all the source code, documentation related to that project).
**The Repository have a ability to set/change the visibility for the users**
## Types of visibility in a Repository-
1. ###### Public Repository:
    - This type of repository is visible to everyone who will visit GitHub website.
    - Anyone can fork the public repository.
    - The changes will be published as activity.
2. ###### Private Repository:
    - This type of repositary will not be visible to everyone who will visit the GitHub, only the publisher of that repository can see and access it.
    - None will able to fork the repository.



# Clone 
Clone is used to copy of the existing repository in a new directory, at another location or we can say bring a repository that is hosted on GitHub into a folder on our local machine.
## Cloning a repository: 

 1. On gitHub, navigate to the main page of repository you want to clone.
2. Above the list of the files, inside the repository, click to **code**.
3. Now, to clone a repository we can use 3 methods, i.e 
        - Using HTTPS, under "Clone with HTTPS".
        - Using SSH Key, which includes a certificate issued by the SSH certificate authority.
        - Using GitHub CLI(zip-folder).
4. If we Use HTTPS and SSl Method to clone we will open Git Bash.
5. Type ` git clone`, then paste the URL you copid earlier.

    ` $ git clone https;//github.com/your_username/your_repositor`

6. Press **Enter** to create your local clone.


# Commit
Commit is to save the changes that we made in the repository in Git.
Through Commit will let the Git To know and save the changes we made to the repository.
Commit can be done using ` git commit` command. it is a good practise to use `-m` with the command that helps to write a meassage related to the commit we made.

` $ git commit -m "Commit-message"`

## How to change the Commit Message
We can change the message of the commit command with the following command,

` $ git commit --amend -m "Updated-message"`



# Git Branching
In Git, A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process.

## Types of Branches:
1. ###### Master Branch:
Master branch is the default or the main branch in a repository.

2. ###### Featured Branch:
Featured Branch are the number of Branches which are made mainly by the team members of a team those are working on the same repository, who are working of the various stages of source code.

3. ###### Hot-fix Branch:
Hot-Fix branches are the branches through which bugs are fixed in the Source code.

![](C:\Users\yamin\Desktop\scam\crownstack\git_assignment/branch.png)

## Commands related to Branch
| Command | Description |
| --- | --- |
| git branch [branch_name] | To create a new Featured branch |
| git branch -a | To list all thr branches |
| git checkout [branch_name] | To switch the branch |
| git branch -d [branch_name] | To delete a branch |
| git push origin --delete [branch_name] | To delete a remote branch |
| git checkout -b [branch_name] | To create a new branch and switch to it |
| git checkout - | To switch to branch last checked out |

## Merging Branches
Git merging is used to merge 2 branches together. It joins two or more developement history together. Merging take place with `git merge ` command.
###### Merging to master branch:
1. To merge a specified commit into master, first discover its commit id. Use the log command to find the particular commit id.

    ` $ git log`

    shows the log with all details done in repository.
2. To merge the commits into the master branch, switch over to the master branch to perform merging operation.
    
    ` $ git checkout master`

3. Use the git merge command along with master branch name. The syntax for this is as follows:
    
    ` $ git merge [id_of branch]`

**NOTE-** To check if merging take place go to the featured branch which we tries to merge and type ` git status`. It will reflect all the changes done in/with that branch. 

## Merge Conflict/Git Conflict
When two or more branches tries to merge, and both are edited at same time and in same file, Git will not be able to identify which version is to take for changes. this situation in Git is known as **Merge Conflict**.

## How conflict can be resolve?
To resolve conflict, it is necessay to know whether the conflict occurs and what is the reason of conflict.

1.  If working in a team with multiple member it's    recommended the `pull` command with `--rebase` option. In short meaning of the command is fetch, Merge, Pull, and Rebase.
    - **Fetch:** Fetching is what we do when we want to see what other have been working on. Fetched content is represented as a remote branch and has no affect on your local development work. More specific `Git fetch` imports the changes from a remote repository (GitHub) and place them in our local repository. When we are fetching, git tells us where it stores each branch on remote repository it fetches.For example:

    ` [id of the file] master -> origin/master `

    This means that `origin/master` stores where `master` is on `origin` repository.This information is then left for `merge` operation.
    - **Merge:** `Git merge` joins 2 or more development histories together. 
    - **Pull:** `Git pull` is the combination of `git fetch` and `git merge`. `git pull` runs `git fetch` with given parameters and then calls `git merge` to merge the retrieved branch heads into the current branch.
    - **Rebase:** `Git merge` takes all the changes and merges them in one commit, while `git rebase` makes the point of any local merge the beginning of the master branch.
    **This means that the commits that you pull will always be at the head of the master branch which is important when many people are committing and pulling because it keeps the branches history clean, linear, and very easy to fix with a rollback in case of any mistakes.**

2. To accept the changes, use a ` git rebase ` command. Git will rewind (undo) all of your local commits, pull down the remote commits then replay your local commits on top of the newly pulled remote commits. If any conflicts arise that git can’t handle you’ll be given the opportunity to manually merge the commits then simply run `rebase` command `with continue` to carry on replaying your local commits.
    
    ` $ git rebase --continue`

This will resolve the conflict and local repository is synchronized with a remote repository.



# What is Origin
Origin is a alias for the remote repository that a project was originally cloned from.
In short, when we type `git remote add origin [URL]`, we are telling our local git that whenever we use the word **origin** we actually means the URL that we specified.
## Commands:
| Command | Description |
| --- | --- |
| git remote add add origin [repository-URL] | Will add  the provides URL to origin |
| git remote -v | To check the list of Remote Repository URLs |



# Pull Request
Pull requests let you tell others about changes you've pushed to a branch in a repository on GitHub.
Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the base branch.
## Commands:
| Command | Description |
| --- | --- |
| git pull | Update local repository to newest commit |
|git pull origin [branch_name] | Pull changes from a remote repository |

**Alternative method:** Pull request can directly be done from GitHub.



# Tags
Tags make a point as a specific point in Git history(marking point). Tags are used to mark a commit stage as relevant.
We can tag a commit for future reference. 
## Types of tags:
1. ###### Annotated Tags:
    - Annotated tags are tags that store extra Metadata like name, email, date, time and more.
    - If we are pointing or saving a final version of any repository, then it is recommended to create an annotated tag.
    - **Command to create annotated tag**

    `$ git tag [tag_name] -m "tag_message"`
2. ###### Light-Weighted Tags:
    - It doesn't save any unnecessary information. Thats the reason of name light-Weighted.
    - If you want to make a temporary mark point or don't want to share information, then you can create a light-weight tag.
    - No command-line options are given to Light-weighted tags.

    `$ git tag [tag_name]` 

## Commands related to tags
| Command | Description |
| --- | --- |
| git tag [tag_name] | To create a tag |
| git tag show [tag_name] | To display details particular tag |
| git push origin [tag_name] | To push the specified tag name as a release point |
| git push --tags | to push all available tags from local repository to remote repository |
| git tag --d [tag_name] [tag_name] | To delete multiple tags |
| git push origin -d [tag_name] | to delete a tag from the remote server |
| git tag [tag_name] [reference_of_commit] | to create a tag for older commit |



# Git Stash
- Git stash is used to store the changes, when they are not be committed and we need to change to a different branch. Simply we can say **git stash** temporarily shelves changes we  made to our working copy, so we can work on something else, and come back and re-apply them later on(switch context).
- Git stash is means as a *temporary storage*.
- Stashing can be done by ` git stash ` command.

    `$ git stash save "someMessage"`
- Every time we save a stash it get stacked so by using `list ` we would be able to see all the saved stashes.

    `$ git stash list`
- **We can get back stash contect by `pop` command.**

    `$ git stash pop`

- We have to remove our stack manually, by `drop`.
    
    `$ git stash drop`

- We can clear all history, using `clear` command.

    `$ git stash clear`

###### Git Stash workflow:
1. Modify a file
2. Stage file
3. Stash it
4. View our stash list
5. Confirm no pending changes through status
6. Apply with pop
7. View list to confirm changes

```
git add .
git stash save "someMessage"

git stash list
git status

git stash pop 
git stash list 
git status
```



*Thanks For reading, Have a good day!* :slightly_smiling_face: