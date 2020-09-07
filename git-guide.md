---
layout: default
title: Getting Started with Git and GitHub
author: Roper
---

[Return to all Guides](/guides.html)

# Getting started with Git and GitHub

This page contains some introductory information on using Git and GitHub, as well as some tutorials for how to use it.

## The difference between Git and GitHub

[Git](https://git-scm.com/) is a distributed version control system. It is used to keep track of all changes in source code, and to allow eaiser
collaboration when writing code.

[GitHub](github.com) is a website that allows users to store their source code. The code is stored using Git. This allows for source
code to be stored in the cloud, with the change tracking and collaboration capabilities of Git.

## Some Basic Terminology

A Git *repository* is a collection with all of the code for a project. On your computer, it is just a folder with some
special stuff going on behind the scenes when you interact with it using Git. After editing files in the repository, you
take a snapshot of the repository called a *commit*. Git keeps track of all of the commits made to the repository,
allowing for changes in files to be tracked.

Futhermore, the commits are in a collection called a *branch*. Additional branches can be created, breaking off of the
current branch, and can later be rejoined with original branch through a function called a *merge*. With GitHub, merges
are created with something called a *pull request*. This will be covered in more detail later on.

A user can *fork* an existing repository. This creates a complete copy of the repository (all commits and
branches) under their own account. This allows them to make their own edits. Once again, *pull requests* are used to
merge a fork back into the original source.

The process of downloading a Git repository from a remote server (such as GitHub), is called *cloning* the repository.
Once cloned, a repository is on the users computer, and new commits added can be *pushed* to the remote server, while
new changes that are added to the server can be downloaded by *pulling* them.

## Tutorials

For start, read [GitHub's documentation on the flow of git](https://guides.github.com/introduction/flow/). This will
give you a good visual overview of how Git works on a basic level.

After that, jump in with the [hello world](https://guides.github.com/activities/hello-world/) tutorial, which will walk
you through the process of creating your own repository on GitHub, creating a new branch, making some changes, and then
re-integrating the branch back into the  main code. Then read
[this guide on forking repositories](https://guides.github.com/activities/forking/), which will have you fork a
repository make some edits, and request for the changes you made to be re-integrated back into the original repository.
This last one is very important, as it is how we will be able to keep track of who does what on the source, and keep
track of proposed changes.

Once you have completed these tutorials, you know how to use most of the features that you will need to work with Git
and GitHub. If you want to see a deeper dive into how to use Git, you can read the
[Git Handbook](https://guides.github.com/introduction/git-handbook/) from GitHub, or the
[complete documentation](https://git-scm.com/doc) on Git. These guides focus on using Git through the command line, but
as the next section will show you,  that is not necessary to use Git.

More tutorials on how to use everything that GitHub offers can be found in the
[GitHub Guides](https://guides.github.com/) or the [GitHub Documentation](https://docs.github.com/en).

## Sofware for working with Git and GitHub

### Installing Git

If you use a computer running Linux, you can install Git through your favorite package manager.

If you want to install just the command line program on Windows or Mac, you can download an installer on the
[official Git website](git-scm.com).

However, the eaisest way to install (and get started with) Git is probably by downloading GitHub Desktop.

### GitHub Desktop

GitHub has made a program that makes using Git on your computer (Windows, Mac, and Linux) a lot eaiser than having
to use the command line. While it lacks a few of Git's more advanced features, it covers (in my experience) pretty much
everything you will need to do on a daily basis. Download it from [https://desktop.github.com/](https://desktop.github.com/).

Once you download it and launch it for the first time, it will give you a quick (~5 minute) tutorial on how to use it.

### Other Software

There are other desktop programs for working with Git available. Because of how Git is written, they should all work
fine with GitHub.

Additionally, a lot of code editor and complete integrated development environments have Git built in now, so you can
manage your project through Git wihtout having to leave your favorite editor.