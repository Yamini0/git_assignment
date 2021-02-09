# Cheatsheet for GIT Commands


Starting with Git. First thing we have to Configure your Git.


# Installation
Write the following command in terminal.

**NOTE:** Git should be available in the standard system repository, like Linux or Ubuntu
- *For Standard Systems:*

    ` $ sudo apt-get install git`

- *For Windows operating systems:*
    Download the latest version of Git from [Downloading-link](https://git-scm.com/download/win).

- *For MAC operating systems:*
    Mainly Mac does also have Git pre-installed in it. If not just go with this [Downloading-link](https://git-scm.com/download/mac).


# Git Configuration

| Command | Description |
| --- | --- |
| git config --global user.name ["name"] | Set name that will attached to commits and tags |
| git config --global user.email ["email_address"] | Set e-mail that will attached to commits and tags |

# Creating/Beginning the Project

| Command | Description |
| --- | --- |
| git init [project_name] | Create a new local repository |
| git clone [project_URL] | Clone the repository/project with entire history from remote repository to local repository |

# Some Common Commands

| Command | Description |
| --- | --- |
| git status | Check the status |
| git add ./[file_name] | Add all/a file to the satging area |
| git add -A | Add all new & changed files to the staging area |
| git commit -m "[commit_meassage]" | Commit the changes to Git |
| git reset [file_name] | Revert repository to previous work state |
| git reset --hard [file_name] | All changes are discard |
| git rm -r [file_name] | Remove the file from working directory/staging area |
| git stash | Put current changes in your **working directory** into **stash** for later use |
| git stash pop | Apply stored stas to working directory and clear the stash |
| git stash drop | Delete a specific stash |


# Git branching and Merging

| Command | Description |
| --- | --- |
| git branch | List Branches( asterisk denotes the current branch) |
| git branch -a | List all branches(local & remote) |
| git branch [branch_name] | Create a new Branch |
| git branch -d [branch_name] | Delete a branch |
| git push origin --delete [branch_name] | Delete a remote branch |
| git checkout [branch_name] | Switch to particular branch |
| git checkout - | Switch to branch last checked-out |
| git checkout -b [branch_name] | Create a new Branch and switch to it |
| git checkout -b [branch_name] origin/[branch_name] | Clone a remote branch and switch to it |
| git checkout -- [file_name] | discard changes to a file |
| git branch -m [old_branch_name] [new_branch_name] | Rename a branch |
| git merge [branch_name] | Merge a branch into active branch |
git merge [source_branch] [target_branch] | Merge a branch into target branch |
| git stash | Stash changes in dirty working directory | git stash clear | Remove all stashed entries |


# Sharing & Updating Project

| Command | Description |
| --- | --- |
| git push origin [branch_name] | Puch a branch to remote repository |
| git push -u origin [branch_name] | Push changes to remote repositary nad remember the branch |
| git push origin --delete [branch_name] | Delete a remote branch |
| git pull | update local repository to newest commit |
| git pull origin [branch_name] | Pull changes from remote repository |
| git remote add origin [url/ssl] | Add remote repository |
| git remote -v | List all the stored remote repository |
| git fetch [branch] | Fetch changes from remote, but not update tracking branches |
| git fetch --prune [branch] | Delete remote Refs that were removed from the remote repository |


# Review & Comparison

| Command | Description |
| --- | --- |
| git log | View all the changes in repository |
| git log --summary | View changes(detailed) |
| git log --oneline | View changes(briefly) |
| git log ref.. | List changes on the current branch |
| git reflog | List operations made on local repository |
| git log --oneline --graph --decorate | View changes with referenced labels and history graph |
| git diff [source_branch] [target_branch] | Preview changes before merging |


# Tagging

| Command | Description |
| --- | --- |
| git tag | List all tags |
| git tag [tag_name] | Create a tag for current commit | git git tag -d [tag_name] | Delete a tag from local repository |
| git push origin [tag_name] | To push the specified tag name as a release point |
| git push --tags | to push all available tags from local repository to remote repository |
| git tag --d [tag_name] [tag_name] | To delete multiple tags |
| git push origin -d [tag_name] | to delete a tag from the remote server |
| git tag [tag_name] [reference_of_commit] | to create a tag for older commit |



