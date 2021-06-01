---
description: 'Chapter 3: Contributing Guidelines'
---

# Chapter 3

## 3. Contributing Guidelines

## Table of Contents

* 3.1 [Introduction](ch3.md#3-1-introduction)
* 3.2 [Installation](ch3.md#3-2-installation)
  * 3.2.1 [Cloning from VCS](ch3.md#3-2-1-cloning-from-vcs)
  * 3.2.2 [Environment Setup](ch3.md#3-2-2-environment-setup)
  * 3.2.3 [Building from source](ch3.md#3-2-3-building-from-source)
* 3.3 Structure
  * 3.3.1 Repository Structure
  * 3.3.2 Package Structure
* 3.4 Development
  * 3.4.1 Testing & Code Coverage
  * 3.4.2 Documentation
  * 3.4.3 Security
  * 3.4.4 VCS Notes
* 3.5 Contributing to this Manual

### 3.1 Introduction

Epispot is built on open-source contributions and we're glad that you want to contribute. First things first, if you want to contribute you will need the link to the GitHub source: [https://github.com/epispot/epispot](https://github.com/epispot/epispot). All contributions to epispot should be submitted as pull requests on GitHub which we can then merge. In order to facilitate this review process, epispot has created a set of contributing guidelines which you can view [here](https://github.com/epispot/epispot/tree/master/CONTRIBUTING.md). The goal of this page in the manual is to further expand on some of the principles touched on in that document and make it easier to contribute to epispot. Continue reading to learn how to start.

### 3.2 Installation

The installation process for development is just a bit different from the standard installation process. This will make it easier to do testing and code coverage analysis locally, which will be described later. However, you can always perform these on GitHub if you prefer and just install `epispot-nightly` instead with:

```bash
pip install epispot-nightly
```

In this case, you can skip all but the first section of this chapter. However, it will be worth it to build `epispot` from the source as it is easier to run tests and debug your code locally.

#### 3.2.1 Cloning from VCS

If you don't have `git` already, you can install it here: [https://git-scm.com](https://git-scm.com). Epispot uses `git` as its de-facto version control system, so it'll help to get familiar with the fundamentals of `git`. After you have, make sure to learn [the basics of GitHub](https://docs.github.com/en/github/getting-started-with-github/quickstart) so that you understand how to submit your pull request when it's time. The first step will be to fork the GitHub repository by clicking the "Fork" button and creating a copy under your username. Next, clone your local copy with `git` by providing the GitHub URL to your fork like this:

```bash
# replace username with your GitHub username
git clone https://github.com/username/epispot
```

This should create a folder containing the `epispot` codebase. Run the following commands from inside the folder to initialize the repository properly and get it up-to-date:

```bash
git checkout master
git pull
```

Finally, create a new branch to work on locally with:

```bash
git branch name  # replace name with branch name
```

Choose a name that clearly states, in one or two words, what the purpose of the branch is and what it does. Good branch names are short, concise, and descriptive. Here are a few good examples:

```bash
git branch super-coverage  # increases code coverage
git branch pdoc-mako  # adds mako templates to pdoc
git branch docs-overhaul  # recreates documentation
```

If you are working on [fixing an issue](https://github.com/epispot/epispot/issues), use a branch name that specifies the issue number that you are fixing after the `patch` label like this:

```bash
git branch patch-num  # replace num with issue #
```

Now checkout your branch and you're ready to go! The next section will cover how to get ready to install epispot after you've cloned the repo.

#### 3.2.2 Environment Setup

The next thing you'll want to do after cloning the repository is set up a Python [virtual environment](https://docs.python.org/3/tutorial/venv.html#creating-virtual-environments). This will allow you to set up epispot's dependencies in a separate environment from your standard Python installation. The steps to create the virtual environment are listed below for `pip` and `conda` systems:

{% tabs %}
{% tab title="Python" %}
```bash
python -m venv epispot
source tutorial-env/bin/activate

# If the last command returns an error on Windows, run:
# tutorial-env\Scripts\activate.bat
```
{% endtab %}

{% tab title="Conda" %}
```bash
conda create -n epispot anaconda
source activate epispot

# When installing packages, use the below script
# to ensure that they are installed to the `epispot`
# virtual environment:

# conda install -n yourenvname [package]
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Please note that `epispot` is designed for Python 3, and it is ideal that you use a Python version greater than or equal to `3.6` when creating these virtual environments.
{% endhint %}

Now, type `python` into your shell and you should see an interactive shell similar to the one shown below pop up.

```bash
(epispot) $ python
Python 3.7.2 (default, May  6 2016, 10:59:36)
  ...
```

Make sure that the Python installation is greater than or equal to Python `3.6` and that the `(epispot)` virtual environment indicator shows up. Next, you're ready to build `epispot` from the source.

#### 3.2.3 Building from Source

First off, you'll need to install all package dependencies into your virtual environment. If you are using `pip`, just navigate to the root repository directory and type:

```bash
pip install -r requirements.txt  # Install package dependencies
pip install -r bin/requirements.txt  # Install CLI dependencies
```

This will install `numpy`, `matplotlib`, and `fire` for the CLI. Finally, you can build `epispot` from the source `setup-nightly.py` file with:

```bash
python setup-nightly.py develop
```

This will create a symbolic link to the package that will prevent you from constantly re-installing `epispot`. However, if you would like to reinstall `epispot` every time a change is made and keep a stable `epispot` installation on your computer, you can run:

```bash
python setup-nightly.py install
```

each time you make a change. And that's all! Fire up a shell from anywhere within the repository and import `epispot` with:

```bash
$ python
Python 3.7.2 (default, May  6 2016, 10:59:36)
  ...
>>> import epispot
>>> print(epispot.version)
2.1.1
```

 ✨🍰✨ Congratulations!



