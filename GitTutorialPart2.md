# Git Tutorial Part 2

### 7. git checkout

Updates files in the working tree to match the version in the index or the specified tree. If no pathspec is given, git checkout will also update HEAD to set the specified branch as the current branch.

`git checkout [<branch>]`

_This command is used to switch from one branch to another._

`git checkout -b [<branch>]`

_This command is used to create and switch to the created branch._

![Checkout Screenshot.](image/checkoutImage.png)

Detailed description of the command `git checkout` can be found [here](https://git-scm.com/docs/git-checkout).

### 8. git push

| Command                             |                                        Usage                                         |
| ----------------------------------- | :----------------------------------------------------------------------------------: |
| `git push [variable name] main`     | This command sends the committed changes of master branch to your remote repository. |
| `git push [variable name] [branch]` |           This command sends the branch commits to your remote repository.           |
| `git push –all [variable name]`     |             This command pushes all branches to your remote repository.              |

![Push Screenshot.](image/pushImage.png)

Detailed description of the command `git push` can be found [here](https://git-scm.com/docs/git-push).

### 9. git pull

`git pull [<options>] [<repository> [<refspec>…​]]`

Incorporates changes from a remote repository into the current branch. In its default mode, git pull is shorthand for `git fetch` followed by `git merge FETCH_HEAD`.

![Pull Screenshot](image/pullImage1.png)

Detailed description of the command `git pull` can be found [here](https://git-scm.com/docs/git-pull).

### 10. git remote add/ remove/ show

- `git remote add`

_Add a remote named `<name>` for the repository at `<url>`. The command `git fetch <name>` can then be used to create and update remote-tracking branches `<name>/<branch>`._

- `git remote rm <name>`

_Remove the remote named `<name>`. All remote-tracking branches and configuration settings for the remote are removed._

- `git remote show <name>`

_Gives some information about the remote `<name>`._

Detailed description of the command `git remote` can be found [here](https://git-scm.com/docs/git-remote).

### 11. git status

This command lists all the files that have to be committed.

![Status Screenshot.](image/StatusImage.png)

Detailed description of the command `git status` can be found [here](https://git-scm.com/docs/git-status).

### 12. Master Branch / Main Branch

_A branch in Git is simply a lightweight movable pointer to one of the commits. The default branch name in Git is master (now, "main"
). As we start making commits, we’re given a master(main) branch that points to the last commit we made. Every time we commit, the master(main) branch pointer moves forward automatically._

_The “master / main” branch in Git is not a special branch. It is exactly like any other branch._
