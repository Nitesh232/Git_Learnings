## Creating Git folder 

In Git, you can make a new directory (also called a folder) using the mkdir command. This command takes the name of the directory you want to create as an argument. For example, if you wanted to create a directory called "my-project", you would run the following command:

`mkdir my-project`

This would create a new directory called "my-project" in your current working directory.

To change to a different directory in Git, you can use the cd command. This command takes the name of the directory you want to change to as an argument. For example, if you wanted to change to the "my-project" directory that you just created, you would run the following command:

`cd my-project`

**Note:** If you already have a folder/directory you would like to use for Git:

Navigate to it in command line, or open it in your file explorer, right-click and select "Git Bash here".

## Creating, listing and removing file.

In Git, you can add files to your repository, list the files that are currently tracked, and remove files from your repository using a few different commands. Here are some of the most common commands for working with files in Git:

#### Adding files

To add a file to your repository, you can use the git add command. This command takes the name of the file you want to add as an argument. For example, if you wanted to add a file called "myfile.txt", you would run the following command:

`git add myfile.txt`

If you have multiple files you want to add, you can use a wildcard (*) to add all files in a directory:

`git add *`

Note that adding a file only stages it for the next commit. You'll need to use the `git commit` command to actually commit the changes to your repository, we will see `git commit` later below soon.

#### Listing files

To see a list of the files that are currently being tracked by Git, you can use the `git ls-files` command. This command lists all the files in the repository, including any subdirectories. For example, to list all files in your repository, you would run:

`git ls-files`

You can also use `ls` command to list folders and files present in the same directory.

Use `ls -a` command to show .git folder. (ls won’t show you the .git folder, but ls -a will)

#### Removing files

To remove a file from your repository, you can use the `git rm` command. This command takes the name of the file you want to remove as an argument. For example, if you wanted to remove a file called "myfile.txt", you would run the following command:

`git rm myfile.txt`

Note that this command will also delete the file from your local filesystem. If you just want to remove the file from Git, but keep a copy on your local filesystem, you can use the --cached option:

`git rm --cached myfile.txt`

This will remove the file from Git's index, but leave it on your local filesystem.


## Git commit

after running `git add` or `git rm` commands, you need to run the `git commit` command to actually commit the changes to your repository.

The `git add` command stages changes in your working directory and adds them to the index (also known as the staging area). However, this only prepares the changes to be committed. To permanently save the changes to your repository, you need to create a new commit.

The `git commit` command creates a new commit with the changes that are currently in the index. When you run this command, Git opens a text editor where you can enter a commit message that describes the changes you've made.

Here's an example workflow for adding a new file to your repository:

    1. Create a new file in your working directory: `touch newfile.txt`.
    2. Stage the file for commit: `git add newfile.txt`.
    3. Commit the changes: `git commit -m "Added a new file"`.


And here's an example workflow for removing a file from your repository:


    1. Remove the file from your working directory: `rm myfile.txt`.
    2. Stage the removal for commit: `git rm myfile.txt`.
    3. Commit the changes: `git commit -m "Removed a file"`.


In both cases, the `git add` or `git rm` command stages the changes, and the `git commit` command creates a new commit with those changes.


In Git, files are managed and tracked using a system of snapshots. When you make changes to a file in your repository, Git creates a new snapshot of that file, and keeps track of its history over time.

There are a few different stages that files can go through in Git:

-  **Untracked:** When you create a new file in your repository, or if you've made changes to a file that Git isn't currently tracking, that file is considered untracked. You can use the `git status` command to see which files are currently untracked.

- **Staged:** Before committing changes to a file, you must stage it by using the `git add` command. Staging a file tells Git that you want to include it in the next commit.

- **Committed:** When you commit changes to a file, Git takes a snapshot of that file and stores it in the repository's history. You can add a message to describe the changes you've made by using the `-m` option with the `git commit` command.

Some common Git commands for working with files include:

- `git status:` Shows the current status of the repository, including which files have changes that are staged or unstaged.
- `git diff:` Shows the differences between the current version of a file and the previous version in the repository.
- `git log:` Shows the history of commits in the repository, including the commit messages and the files that were changed.


It's important to note that Git doesn't just track the contents of files, but also their names and paths. If you rename or move a file, Git will keep track of that change and include it in the repository's history.

Git also allows you to work with multiple branches, which can be useful for developing new features or experimenting with different versions of your code. When you switch between branches, Git will update the files in your working directory to match the state of the repository for that branch. We will see this in our next notes [here]().

