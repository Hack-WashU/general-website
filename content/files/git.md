---
title: "Git Workflow & Environment Setup"
draft: false
---

# Git Workflow Tutorial

Hey! Thanks for wanting to help out with tech. This document will outline our general workflow, and help you get set up to contribute to our projects.

## Platform-Specific Differences (Windows)

Sadly, this document also must go over environment setup. Generally, we try to make things as easy as possible through tools like [GNU Make](https://www.gnu.org/software/make/) and [Docker](https://www.docker.com/).

These tools work out of the box on MacOS/Linux, but require a good amount of configuration on Windows. For this reason, I'm going to assume you're using WSL, or Windows Subsystem for Linux. This is a fantastic tool, and it makes setting up standardized development environments *significantly* easier.

To get set up with WSL, follow this [Installation tutorial](https://learn.microsoft.com/en-us/windows/wsl/setup/environment). If you're not familiar with Bash, run through this (very quick) [Bash tutorial](https://learn.microsoft.com/en-us/windows/wsl/tutorials/linux).

Docker is another tool tool that we're going to use to emulate both production and dev environments. Sadly, Docker requires a Windows pro license to access the hypervisor, but WashU gives every student a free Windows for Education key, which has the same features as Pro! You can get your license key from [OnTheHub](https://wustl.onthehub.com/WebStore/OfferingDetails.aspx?o=32f87f43-c83a-e511-940f-b8ca3a5db7a1), and follow [these](https://support.microsoft.com/en-us/windows/upgrade-windows-home-to-windows-pro-ef34d520-e73f-3198-c525-d1a218cc2818) steps to change your product key.

> Note: You don't have to necessarily upgrade Windows yet! We'll mention later in the tutorial when you need to launch a Docker container. There also should also be an option to run each project locally if you don't want to upgrade Windows or can't get a key.

## MacOS

Nothing much here! This tutorial is going to assume you have [homebrew](https://brew.sh/) set up. If you'd like a fancier terminal, check out [iTerm2](https://iterm2.com/), or [Warp](https://www.warp.dev/) if you want to get *really* crazy.

# The Meat & Potatoes

Time to set up git! If you don't have it installed, here's their [install](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) page. If you're on Windows, follow the Linux instructions while in your WSL terminal. If you're on MacOS, just run `git` in terminal and it should prompt you to install xcode developer tools. You should also go ahead an install [Visual Studio Code](https://code.visualstudio.com/) (Even if you're using WSL, make sure to still install the Windows version -- see [here](https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode) to get set up).

I would also *highly* recommend both the [Github CLI](https://cli.github.com/) and the [Github Desktop](https://desktop.github.com/) app. If you're new to git, these make contributing significantly easier. (Linux CLI install docs can be found [here](https://github.com/cli/cli/blob/trunk/docs/install_linux.md))

> Note: When setting up the Github CLI, you'll be asked when you run `gh auth login` to select your preferred option of SSH or HTTPS. **Make sure to choose SSH**. You'll also be asked whether or not you want to create a public key and add it to your Github account. If you have no idea what this means, **select Yes**. Make sure not to include a passphrase.
>
> If you have an existing public key, it's up to you whether or not you want to create a new one specifically for your Github account.

### Forking, Cloning, and Editing!

Time to clone the repository! Run `gh repo fork hack-washu/git-tutorial`. This creates a copy of the repository in your Github account. You can also do this manually by clicking the fork button at the top right of the [repo on Github](https://github.com/Hack-WashU/git-tutorial).

> You can't clone & push to the original repository without being a member of the Hack-WashU github repository. We'll add you later, this is just to get started.

After cloning, `cd` into the repository and run `code .`. This should open up a VSCode window with the repository! You should be able to see everything in the repository in the side window. You can open a terminal in VSCode by pressing `CMD/CTRL + ~`.

### Your First Commit

In the repository you just cloned, see what happens when you run `make`. You should get an output of all of the scripts in the Makefile. If you don't, you may need to install make on your system.

At this point, you need to install Node.JS. If you're on Mac, do so with `brew install node`.

> If you're using WSL/Linux, the version bundled with apt is out of date. Follow [this](https://learn.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-on-wsl#install-nvm-nodejs-and-npm) guide to install Node through the node version manager, and install the LTS version.

Now try running `make install` in your VSCode terminal. If you don't get any errors, run `make start`. A web browser should open with the Hack WashU logo! Keep this window open.

Look through the files in the react-app directory. Follow these directions:

1. Add your name to the file! Wrap it in a `<p>` tag and an `<a>` tag, adding a link to your Github profile.
2. Give your name (and only your name) some swanky custom styling. [Here's](https://www.w3schools.com/cssref/index.php) a reference.
3. Save your changes, and verify they were hot-reloaded in your browser!
4. Click the source tree button on the left bar of VSCode, type a fun message into the box, and click "Commit".
5. Click "Sync Changes"!

You just pushed your changes to your repository! This should be similar to what you've done in all of the WashU CS classes.

> Note: The above git gui instructions are the same as `git commit -am "<fun message>"` and `git push origin main`.

### Your First PR

You should now have your name on the home page of your fork! Time to merge your changes with the main repository.

1. Go to the [base repository](https://github.com/hack-washu/git-tutorial).
2. Click on the Pull Requests tab, and then "New pull request"
3. If necessary, click "Compare across forks" in the text above the target bar. Make sure it looks something like the following:
    
    `base repository: Hack-WashU/git-tutorial base: main <- head repository: <your name>/git-tutorial base: main`
4. Click "Create pull request"
5. Fill in any information requested by the pull request template
6. Click "Create pull request"!
7. Assuming you have no merge conflicts, click the big green Merge button!
