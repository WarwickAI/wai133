# WAI133

A swift introduction to GitHub and collaborative programming in Python.

## Contents

- [WAI133](#wai133)
  - [Contents](#contents)
  - [TLDR](#tldr)
  - [Introduction](#introduction)
  - [Setup](#setup)
    - [Downloads](#downloads)
    - [Git](#git)
    - [VS Code](#vs-code)
    - [VS Code Extensions](#vs-code-extensions)
  - [GitHub Resources](#github-resources)
  - [Modern Python Programming](#modern-python-programming)
    - [Context](#context)
    - [Solution: Conda and Poetry](#solution-conda-and-poetry)

---

## TLDR

1. Install [VS Code](https://code.visualstudio.com/).
1. Install [Git](https://git-scm.com/downloads).
1. Install [GitHub for Desktop](https://desktop.github.com/) (Optional).
1. Install the [GitHub Pull Requests and Issues](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) extension.
1. Install the [Remote - SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh) extension (Optional).
1. Install [Conda](https://docs.anaconda.com/miniconda/install/) (you likely want miniconda).
1. Create a new conda environment using `conda create -n your-environment-name python=3.12 -y`.
1. Activate the environment using `conda activate your-environment-name`.
1. Install Poetry using `pip install poetry`.
1. Initialise a new project using `poetry init`.
1. Install packages using `poetry add package-name`.
1. When sharing your code, the other person can run `poetry install` to install
   the packages you used.

```bash
# Copy and paste this command block into your terminal after step 6 to create a new project.
ENVNAME=your-environment-name
conda create -n $ENVNAME python=3.12 -y
conda activate $ENVNAME
pip install poetry
poetry init -q
```

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

## Setup

Before getting to the contents of the tutorial, I'd like to discuss how to get
the most out of it. The **main parts** of the tutorial will be **at the end** of
this README.md to **encourage** you to have **a suitable environment**.

### Downloads

- [VS Code Download](https://code.visualstudio.com/)
- [Git Download](https://git-scm.com/downloads)
- [GitHub for Desktop Download](https://desktop.github.com/) (Optional) This
  makes the installation of Git easier and provides a GUI for Git.

### Git

[Git Download](https://git-scm.com/downloads)

Git is the backbone of what we're about to do. It provides most of the commands
that VS Code will use in it's neat UI. The setup process might be somewhat
tedious on Windows, but necessary for getting the most out of this tutorial.

You may have to restart your device after installing Git and add it to your
PATH. If you're not sure how to do this, please take the liberty to Google it.

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

- [Optional] [Remote - SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh)
  Super useful if you're working remotely. This extension allows you to
  connect to remote machines using SSH. If your a DCS student, you'll be
  using this extension a lot as you can connect to the DCS servers using SSH.

## GitHub Resources

- [YouTube Video: Using Git & GitHub in VS Code](https://www.youtube.com/watch?v=z5jZ9lrSpqk)

After watching this video, I challenge you to:

1. Clone this repository or clone this repository.
1. Create a new branch, called `add-name-(your-name-here)`. For me it would be
   `add-name-jakub`.
1. Add your name to the list below and commit the changes.
1. Submit a pull request from your branch to the `main` branch.
1. I'll review the pull request and merge it in.

---

Names added:

- Jakub

---

## Modern Python Programming

This section will not teach you Python, instead it will provide you with a good
environment to share your Python code with others and collaborate on projects.
At WAI, we do this a LOT.

### Context

Now, you might think that "send me the code" is a good way to share code. It
certainly does the job, but cetrainly has some downfalls.

- That code has dependencies (from all of those `pip install` commands), and
those dependencies have dependencies.
- You might be using a different version of a dependency than your friend, or
even a different version of Python.
- Oh and not to mention historically installing multiple versions of Python has
been a **disaster!**
- You might be using different (or versions of) managers for your dependencies
  (e.g. `pip`).

Do you see where this is going? Sharing code is not as easy as it seems.

The benefit of Python is that it is very flexible, but this is also a downside
when it comes to sharing code. This is where virtual environments come in.

A **virtual environment** attempts to isolate your code from the rest of your
system. When is comes to Python, this can be done in multiple ways. The
recommended way is to use `conda` environments. You can also use `venv` or
`virtualenv`, but we will not be covering those in this tutorial.

A **package manager** is a tool that allows you to install, update and remove
packages (or libraries) from your environment. The most common package manager
for Python is `pip`. `conda` also has it's own package manager, but has flaws
due to most people supporting `pip`. `pip` unfortunately also has major flaws in
that it handles what dependencies are installed, but not which ones are required
for a project. This is where `requirements.txt` files come in. These files list
all of the dependencies for a project, allowing you to install them all at once.
However, this is not a perfect solution as it does not handle versioning well.
It is also very much a **manual process** and a pain to keep up to date.

### Solution: Conda and Poetry

#### Download Conda

[Conda Download](https://docs.anaconda.com/miniconda/install/)

Testing your installation:

```bash
conda --version
```

If you get a version number, you're good to go, if not, please check your PATH
and restart your device. If you're still having issues, feel free to ask for
help in the WAI Discord server.

#### Conda Environments

Alright, now with conda installed, we can create a new environment. This is done
using the following command:

```bash
conda create -n your-environment-name python=3.12 -y
```

I highly recommend using the `python=3.12`. Older versions of Python (especially
before 3.10) run much slower and might even lead to using more RAM and GPU
memory due to older libraries not being optimised. `-n` or `--name` is the name
of the environment you want to create, so replace `your-environment-name` with
anything you like. `-y` automatically accepts the installation of the packages
required for the environment.

After creating the environment, you can activate it using the following command:

```bash
conda activate your-environment-name
```

You should see the name of the environment in your terminal prompt. This means
that you are now in the environment and can install packages to it.

#### Poetry

Now that we are in a conda environment, we can install `poetry`. Poetry will
handle what version of packages you installed for your current project.

```bash
pip install poetry
```

Now that you have `poetry` installed you can run:

```bash
poetry init
```

which will initialise a new project in the **current directory**. Next time you
want to install a python package do the following:

```bash
# Instead of `pip install numpy`
poetry add numpy
```

Then the person who you share your code with can clone your GitHub repository
and run the following command to sync up:

```bash
# conda create -n your-environment-name python=3.12 -y
# conda activate your-environment-name
poetry install
```
