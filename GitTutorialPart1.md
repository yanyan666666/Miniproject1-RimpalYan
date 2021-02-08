#**Git Tutorial Part1**#

##**1.Repository**##

A repository is the most basic element of GitHub. They are easiest to imagine as a project's folder.
A repository contains all of the project files(including documentation), and stores each file's revision history. Repositories can have multiple collaborators and can be either public or private.

##**2.Clone**##

A clone is a copy of a repository that lives on your computer instead of on a website's server somewhere, or the act of making that copy.

##**3.Fork**##

A fork is a personal copy of another user's repository that lives on your account. Forks allow you to freely make changes to a project without affecting the original upstream repository. You can also open a pull request in the upstream repository and keep your fork synced with the latest changes since both repositories are still connected.

##**4.Branch**

###**4.1 Definition**

A branch is a parallel version of a repository. It is contained within the repository, but does not affect the primary or main branch allowing you to work freely without disrupting the "live" version.

###**4.2 Application**

$git branch *branch A*<br>
You will create a new branch named"branch A".

##**5.Commit**

###**5.1 Definition**

A commit, or "revision", is an individual change to a file (or set of files). When you make a commit to save your work, Git creates a unique ID (a.k.a. the "SHA" or "hash") that allows you to keep record of the specific changes committed along with who made them and when.

###**5.2 Application**

$git commit -m*'Task: added tutorial page'*<br>
You will create a commit with message.

##**6.Merge**

###**6.1 Defination**

Merging takes the changes from one branch (in the same repository or from a fork), and applies them into another. This often happens as a "pull request" (which can be thought of as a request to merge), or via the command line.

###**6.2 Application**

$git merge *main*<br>
The current commit will merge to main.
![Merge commit](/merge.png)
