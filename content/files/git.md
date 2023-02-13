---
title: "Git Workflow Tutorial"
draft: true
---

# Git Workflow Tutorial

Hey! Thanks for wanting to help out with tech. This document will outline our general workflow, and help you get set up to contribute to our projects.

## Platform-Specific Differences (Windows)

Sadly, this document also must go over environment setup. Generally, we try to make things as easy as possible through tools like [GNU Make](https://www.gnu.org/software/make/) and [Docker](https://www.docker.com/).

These tools work out of the box on MacOS/Linux, but require a good amount of configuration on Windows. For this reason, I'm going to assume you're using WSL, or Windows Subsystem for Linux. This is a fantastic tool, and it makes setting up standardized development environments *significantly* easier.

To get set up with WSL, follow this [Installation tutorial](https://learn.microsoft.com/en-us/windows/wsl/setup/environment). If you're not familiar with Bash, run through this (very quick) [Bash tutorial](https://learn.microsoft.com/en-us/windows/wsl/tutorials/linux).

Docker is another tool tool that we're going to use to emulate both production and dev environments. Sadly, Docker requires a Windows pro license to access the hypervisor, but WashU gives every student a free Windows for Education key, which has the same features as Pro! You can get your license key from [OnTheHub](https://wustl.onthehub.com/WebStore/OfferingDetails.aspx?o=32f87f43-c83a-e511-940f-b8ca3a5db7a1), and follow [these](https://support.microsoft.com/en-us/windows/upgrade-windows-home-to-windows-pro-ef34d520-e73f-3198-c525-d1a218cc2818) steps to change your product key.

> Note: You don't have to necessarily upgrade Windows yet! We'll mention later in the tutorial when you need to launch a Docker container. There also should also be an option to run each project locally if you don't want to upgrade Windows or can't get a key.
