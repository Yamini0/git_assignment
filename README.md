# What is Git?

Git is free,open-source software distributed version control system, commonly known as DVCS, that is designed to manage all the source code history.
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
    - Noone will able to fork the repository.


# Clone 
Clone is used to copy of the existing repositary in a new directory, at another location or we can say bring a repository that is hosted on GitHub into a folder on our local machine.
## Cloning a repository
we can clone a repository in 2 ways:
1. ## Using GitHub:
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

# How to change the Commit Message
We can change the message of the commit command with the following command,
` $ git commit -amend _m "Updated-message"`



# Git Branching
In Git, A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process.

## Types of Branches:
1. ###### Master Branch:
Master branch is the default or the main branch in a repository.
2. ###### Featured Branch
Featured Branch are the number of Branches which are made mainly by the team members of a team those are working on the same repository, who are working of the various stages of source code.
3. ###### Hot-fix Branch
Hot-Fix branches are the branches through which bugs are fixed in the Source code.

## How to make Branch:
`git branch [branch_name]`

### How to Change branch:
`git checkout [branch_name]`


