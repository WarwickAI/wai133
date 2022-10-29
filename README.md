# WAI133

A swift introduction to GitHub.

## Contents

1. [Introduction](#Introduction)
1. [Setup](#Setup)
<!-- 1. [Repositories](#Repositories) -->
<!-- 1. [Branches](#Branches) -->
<!-- 1. [Committing Changes](#Committing-Changes) -->
<!-- 1. [Pushing Changes](#Pushing-Changes) -->
<!-- 1. [Pulling Changes](#Pulling-Changes) -->
<!-- 1. [Merging](#Merging) -->
<!-- 1. [Pull Requests](#Pull-Requests) -->
<!-- 1. [Issues](#Issues) -->
<!-- 1. [About Me](#About-Me) -->
<!-- 1. [Resources](#Resources) -->

---

## Introduction

You may be asking what is GitHub and why should I use it?

GitHub is a version control platform using Git and is a great way to collaborate
with others on projects. It allows everyone to keep track of changes made to the
code, who made them and when. It also allows you to revert back to previous
versions - handy if you make some terrible mistakes... ;(

A great benefit of GitHub is that it is free for public repositories, allowing
you to share your code with others without much overhead.

Note: I have been using my VS Code instalation for a while now, so I may have
missed some steps due to the amount of extensions that do a lot of this for me
now. If you find any, please let me know :)

---

## Setup

Before getting to the contents of the tutorial, I'd like to discuss how to get
the most out of it. The **main parts** of the tutorial will be **at the end** of
this README.md to **encourage** you to have **a suitable setup**.

### Downloads

- [VS Code Download](https://code.visualstudio.com/)
- [GitHub for Desktop Download](https://desktop.github.com/)

<!-- TODO(JakubCzarlinski): Add images -->

### Git

[Git Download](https://git-scm.com/downloads)

Git is the backbone of what we're about to do. It provides most of the commands
that VS Code will use in it's neat UI. The setup process might be somewhat
tedious on Windows, but necessary for getting the most out of this tutorial.

You may have to restart your device after installing Git and add it to your
PATH.

### VS Code

[VS Code Download](https://code.visualstudio.com/)

My text editor of choice is ~~notepad.exe~~ **VS Code**. It loads fast and I
find that for most project I don't need anything else. As well as that, it is
really easy to connect to remote locations, which is handy if you're a DCS
student working remotely. It also integrates well with WSL2 (Windows Subsystem
for Linux) - don't worry about this for now.

VS Code has some amazing extensions that make it even better - we'll be using a
few of them in this tutorial.

### VS Code Extensions

Now that we have VS Code and Git installed, we can install some extensions to
enhance our experience. I'll be using the following extensions:

- [GitHub Pull Requests and Issues](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)
    This extension allows you to create pull requests and issues directly from
    VS Code. We'll be using this to create a pull request for this tutorial.
    You'll also be able to test the extension by creating an issue for this
    tutorial.

- \[Optional\] [SandDance for VS Code](https://marketplace.visualstudio.com/items?itemName=msrvida.vscode-sanddance)
    This extension allows you to visualise data in VS Code. It's truly amazing
    when it comes to visualising datasets in csv and tsv format. If you're
    reading this tutorial, you'll probably find this extension useful at some
    point as you're likely from WAI.

- \[Optional\] [Remote - SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh)
    Super useful if you're working remotely. This extension allows you to
    connect to remote machines using SSH. If your a DCS student, you'll be
    using this extension a lot.

---
