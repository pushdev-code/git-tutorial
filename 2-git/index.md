# Introduction to Git

Git is a popular tool to manage repositories, most companies relay on it or in similar systems.

## What is Git?

Git is an implementation of a distributed [version control system](../1-version-control-systems).

## Installation

Go to https://git-scm.com/downloads and get the correct version for your system.

There are versions for:

* [Ubuntu, Debian and derived systems](https://git-scm.com/download/linux)
* [Fedora, Red Hat and derived systems](https://git-scm.com/download/linux)
* [Windows](https://git-scm.com/download/win)
* [Mac OS](https://git-scm.com/download/mac)

Once installed you'll be able to open a `Terminal` and type the command ```git``` with no errors.

In modern computing terms, `Terminal` normally refers to the intermediate console which relays commands entered by the programmer to the kernel.

## Git Configuration

You can set the Git configuration using the ```git config``` command.

The most basic configuration is to set your name and email:

```
git config --global user.name "Firstname Lastname"
git config --global user.email "your.email@example.org"
```

There are more options within git configuration that you can explore in the [Git's documentation](https://git-scm.com/docs/git-config).


## Git repositories

Repositories are the file location where all the files related to a project are stored.

More specifically the Git repository is the `.git/` folder inside a project, where all the changes made to the files in your project are tracked, building a history over time. Deleting the `.git/` folder will delete the project’s history.

## Working tree

A local repository provides at least one collection of files which originate from a certain version of the repository. This collection of files is called the working tree. It corresponds to a checkout of one version of the repository.

A file in the working tree of a Git repository can have these states:

* __untracked:__ the file is not tracked by the Git repository. This means that the file never staged nor committed.
* __tracked:__ committed and not staged
* __staged:__ staged to be included in the next commit
* __dirty / modified:__ the file has changed but the change is not staged

## Adding files/changes

Once the working tree is modified, the files/changes need to be added to the repository.

This command will include a single file:

```
git add location_of_file
```

This command will include all changes and all files:

```
git add .
```

You can use --help flag to see more command options:

```
git add --help
```

## Commiting

After adding the files and changes, these are saved in the staging area so you can continue working until you've finished.

When the files are commited, they're added permanently to the Git repository.

```
git commit
```

It is a good practice to include a message for the commit so it can be tracked easily.

```
git commit -m "Meaningfull commit message"
```

Follow [these guidelines](https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53) for good commit messages.

## Branches

Git supports branching which means that you can work on different versions of your collection of files. A branch allows the user to switch between these versions so that he can work on different changes independently from each other.

For example, if you want to develop a new feature, you can create a branch and make the changes in this branch. This does not affect the state of your files in other branches. For example, you can work independently on a branch called production for bugfixes and on another branch called feature_123 for implementing a new feature.

To create a new branch named feature_123:

```
git checkout -b feature_123
```

To get the list of local branches:

```
git branch
```

To switch to an already created branch:

```
git checkout feature_123
```

For better naming and practices follow these [branching standards & conventions](https://gist.github.com/digitaljhelms/4287848).

Branches in Git are local to the repository. A branch created in a local repository does not need to have a counterpart in a remote repository.

## Synchronization with remote Git repositories

Git allows the user to synchronize the local repository with other (remote) repositories.

Users with sufficient authorization can send new version in their local repository to to remote repositories via the push operation. They can also integrate changes from other repositories into their local repository via the fetch and pull operation.

To synchronize your local copy of _master_ branch:

```
git push -u origin master
```

To synchronize your local branch _feature_123_ to a remote branch:

```
git push -u origin feature_123
```

## Pull Requests

Pull requests let you tell others about changes you've pushed to a branch in a repository on GitHub. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the base branch.

Source: https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests

In our courses we'll use Pull requests as a way of receiving feedback and completing code challenges.
