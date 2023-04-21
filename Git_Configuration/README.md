## Git Introduction

Git is a version control system that allows you to manage and track changes to your code over time. It was created by Linus Torvalds in 2005 and has since become one of the most popular version control systems in use today.

Git works by creating a repository, which is a directory that stores all of your code and its history. When you make changes to your code, Git tracks those changes and allows you to easily revert to previous versions if necessary. This can be especially useful when working on a project with multiple collaborators, as Git allows everyone to work on the same codebase without interfering with each other's changes.

Some of the benefits of using Git include:

- Version control: Git allows you to easily track changes to your code over time and revert to previous versions if necessary.
- Collaboration: Git makes it easy to collaborate with others on a project and merge changes from multiple contributors.
- Backup: By storing your code and its history in a Git repository, you have a backup of your code that can be restored if your local copy is lost or damaged.
To use Git, you will need to install it on your computer and learn some basic commands.


## Git installation

In order to use Git, you have to install it on your computer. To do this, you can download the latest version on the official website [here](https://git-scm.com/downloads). You can download for your operating system from the options given.

## Git Configurations

Git configurations allow you to customize your Git environment and set preferences for how Git behaves. Git configurations can be set globally or on a per-repository basis.

To set global Git configurations, use the git config --global command followed by the configuration key and value. For example, to set your name and email address, you can use the following commands:

`` git config --global user.name "Your Name"``

``git config --global user.email "youremail@example.com" ``

These settings will be used for all Git repositories on your computer, unless you override them with per-repository configurations.

Per-repository configurations can be set by running git config commands within a repository. These configurations will only apply to that specific repository. For example, you can set a VS Code as default code editor to use for that repository:

`git config core.editor "code--wait"`

#### Checking configuration settings list

You can also view your list of git cammands for Git configurations by running the `git config --list` command. This will show all of your global and per-repository configurations. Below are few list of cammands..

Other useful Git configurations include:

- `core.autocrlf:` Sets how Git handles line endings. This can be set to `true` to automatically convert line endings to the system's default format, `input` to leave them as-is, or `false` to disable line ending conversion.
- `color.ui:` Enables or disables colored output in Git commands. This can be set to `auto` to enable colors if the output is going to a terminal, `always` to always use colors, or `never` to disable colors.
- `alias:` Allows you to define custom Git commands. For example, you could create an alias to run git log with a custom format: `git config --global alias.lg "log --oneline --decorate --all --graph"`.


Git configurations can be a powerful tool for customizing your Git workflow and making it more efficient. By experimenting with different configurations, you can find settings that work best for your needs.


