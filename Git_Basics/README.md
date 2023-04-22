## Git Basics

Before continuing visit [here]() and read notes.

#### Git status

The `git status` command is used to show the current status of your repository. It shows which files are tracked, which files are modified, and which files are staged for the next commit. Here are some common `git status` commands:

- **`git status :-`** This command provides a summary of the current status of your repository, including any changes that have been made but not yet committed. It also shows which branch you are currently on.
- **`git status -s or git status --short :-`** This command provides a more concise summary of the current status of your repository. It shows the status of each file in the working directory as a two-letter code.
- **`git status -v or git status --verbose :-`** This command provides a more detailed summary of the current status of your repository. It shows the status of each file in the working directory and also shows the differences between the working directory and the staging area.
- **`git status -uno or git status --untracked-files=no :-`** This command suppresses the display of untracked files in the working directory.
- **`git status -u or git status --untracked-files=all :-`** This command shows the status of all files in the working directory, including untracked files.

`git status` is a useful command that can help you keep track of changes to your repository and ensure that everything is in order before committing those changes. You should get in the habit of using git status frequently as you work on your projects.

#### Git log

The `git log` command is used to display the commit history of a repository. It shows the list of commits in reverse chronological order, with the most recent commit listed first. Here are some common git log commands:

- **`git log :-`** This command displays the commit history of the current branch in the default format. By default, the commit history is shown in reverse chronological order, with the most recent commit at the top.
- **`git log --oneline :-`** This command shows a more compact version of the commit history, with each commit on a single line. This can be useful when you want to quickly scan the commit history.
- **`git log --graph :-`** This command shows the commit history as a graph, with the branches and merges clearly labeled. This can be useful when you want to visualize the branching and merging history of your project.
- **`git log --author="name" :-`** This command displays the commit history for a specific author. Replace "name" with the author's name to see their commit history.
- **`git log --grep="search term" :-`** This command displays the commit history for commits that contain the specified search term in the commit message.
- **`git log --pretty=format:"%h - %an, %ar : %s" :-`** This command allows you to format the output of git log. The format string can include placeholders for various pieces of information, such as the commit hash, author name, commit date, and commit message.

`git log` is a powerful command that can provide a wealth of information about the commit history of your project. It is important to understand how to use `git log` effectively in order to get the most out of your Git workflow.


#### Git Clone

The `git clone` command is used to create a copy of an existing Git repository. Here are some common `git clone` commands:

- **`git clone <url> :-`** This command creates a copy of the remote Git repository specified by the URL. By default, the clone will be created in a new directory with the same name as the repository.
- **`git clone <url> <directory> :-`** This command creates a copy of the remote Git repository specified by the URL in the specified directory.
- **`git clone --depth <number> <url> :-`** This command creates a shallow clone of the remote Git repository with the specified number of commits. This can be useful when you only need a specific version of the repository and don't want to clone the entire history.
- **`git clone --branch <branch> <url> :-`** This command creates a clone of the remote Git repository with the specified branch checked out. This can be useful when you only need to work on a specific branch of the repository.
- **`git clone --recursive <url> :-`** This command creates a clone of the remote Git repository and also initializes and clones any submodules that the repository may have.


`git clone` is a powerful command that can be used to quickly create copies of Git repositories for collaboration or for personal use. It is important to understand the different options available with `git clone` in order to use it effectively.

#### Git Branch

Git branches are a powerful feature that allow you to work on multiple versions of your code at the same time. Here are some common `git branch` commands:

- **`git branch :-`** This command shows a list of all the branches in your repository. The current branch is highlighted with an asterisk.
- **`git branch <branch name> :-`** This command creates a new branch with the specified name. The new branch will be created at the current commit.
- **`git branch -d <branch name> :-`** This command deletes the branch with the specified name. Note that you cannot delete the branch you are currently on.
- **`git branch -m <new branch name> :-`** This command renames the current branch to the specified name.
- **`git checkout <branch name> :-`** This command switches to the specified branch.
- **`git checkout -b <new branch name> :-`** This command creates a new branch with the specified name and switches to it.
- **`git merge <branch name> :-`** This command merges the specified branch into the current branch. Note that you must be on the branch you want to merge into (typically the master branch) when running this command.


`git branch` is a powerful command that can help you manage your codebase effectively. It is important to understand how branches work in Git and how to use them effectively to make the most of this feature.

#### Git checkout

The `git checkout` command is used to switch between different branches or to navigate the commit history of a repository. Here are some common `git checkout` commands:

- **`git checkout <branch> :-`** This command switches to the specified branch. If the branch does not exist, you will get an error.
- **`git checkout -b <new branch> :-`** This command creates a new branch with the specified name and switches to it.
- **`git checkout <commit> :-`** This command switches to the specified commit. You will be in a "detached HEAD" state, which means you are not on any branch and any changes you make will not be saved in a branch.
- **`git checkout -b <new branch> <commit> :-`** This command creates a new branch with the specified name and starts it at the specified commit.
- **`git checkout -- <file> :-`** This command discards changes made to the specified file since the last commit.


`git checkout` is a powerful command that can help you navigate your codebase effectively. It is important to understand how to use this command correctly in order to avoid losing changes or accidentally switching to the wrong branch or commit.

#### Git Pull

The `git pull` command is used to update your local branch with the changes from a remote repository. Here are some common `git pull` commands:

- **`git pull :-`** This command fetches the changes from the remote repository and merges them into the current branch. It is equivalent to running `git fetch` followed by git merge.
- **`git pull --rebase :-`** This command fetches the changes from the remote repository and rebases the current branch on top of the fetched changes. This is useful if you want to keep a linear history and avoid merge commits.
- **`git pull <remote> <branch> :-`** This command fetches the changes from the specified remote repository and merges them into the specified branch. If no branch is specified, it defaults to the currently checked out branch.


`git pull` is a powerful command that can help you keep your local branch up-to-date with changes from a remote repository. It is important to understand the different options available with `git pull` in order to use it effectively.


#### Git Push

The `git push` command is used to upload local changes to a remote repository. Here are some common `git push` commands:

- **`git push :-`** This command uploads the local changes to the default remote repository and branch. By default, the local changes are merged with the remote changes.
- **`git push <remote> <branch> :-`** This command uploads the local changes to the specified remote repository and branch.
- **`git push --force :-`** This command overwrites the remote branch with the local changes, even if the remote branch has diverged from the local branch. Use this command with caution, as it can cause data loss and conflicts.
- **`git push --set-upstream <remote> <branch> :-`** This command sets the default upstream branch for the current local branch. This is useful if you want to use git push and git pull without specifying the remote and branch every time.


`git push` is a powerful command that can modify the remote repository. It is important to understand the different options available with `git push` in order to use it effectively and avoid data loss or conflicts.