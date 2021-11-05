# Normie's Guide to Installing Linux Within Windows Using WSL

My attempt at onboarding Linux newbies into the community and helping them get
their sea legs in the scary black box. Many men have written this guide before
me, and many have written it better, but this one is mine. 

## Introduction

Windows Subsystem for Linux (WSL), first released in 2016, is a compatibility
layer for Windows that allows you to execute Linux binaries natively within the
Windows operating system. Once set up, you will be able to install a Linux
distribution of your choosing from the Microsoft Store and run it within a
typical terminal emulator environment using the Bash shell. This can be useful
if you are accustomed to working in a UNIX environment, if you require access to
software that is not available or difficult to install on windows, if you want
to avoid the headaches associated with setting up a development environment in
Windows, or if you are a proponent of free and open-source software.

## Instructions

### 1. Installing WSL

Run Windows PowerShell as administrator and execute the
following command:

	> wsl --install

Once the command is finished executing you will be prompted to restart your
system. 

### 2. Installing a Linux Distro

Launch the Microsoft Store from the start menu.
If you are coming off the reboot after installing WSL, you may see a list of
distributions already. Otherwise, you can search 'Linux' and you should see
a wide array of options. I recommend choosing Ubuntu if you are new to Linux.
This is the traditional starting point for new users. Ubuntu has a very large
online community and plenty of resources and support for when things go wrong.
For the sake of this document I will assume you are installing Ubuntu.

### 3. Running Linux for the First Time

Open the start menu and you should find that Ubuntu has been added to your list
of programs. Upon launching it, you will be prompted to set your username and
password. Once these have been set, a setup script will run and you will arrive
at a bash command prompt.

### 4. Getting Started

Now that you have the system set up, you'll want to get
your package manager updated so you can start installing software and making the
system useful for yourself. For Debian-based distros (which includes Ubuntu and
Linux Mint), you'll be using APT to manage your packages. Run the following
command:

	$ sudo apt update

sudo stands for 'super user do', and is the Linux equivalent of 'Run as
Administrator'. Updating the package manager is an administrative task and
requires elevated privileges. Apt is the command for managing packages, and
update is the subcommand for syncing your package manager with the remote
software repositories. This will update the local database of packages that are
available remotely for download. Next, run the following command:

	$ sudo apt upgrade

This command is much like the last one, but this time we are using the upgrade
subcommand to update all packages on the machine to their latest available
versions in the remote repositories. You will now be completely up to date and
ready to install new software.

### 5. Basics of Using a Command Line Interface

WSL, unlike virtualization, does not provide you with a graphical interface for
using Linux. Because of this, you will need some familiarity with using a
command line interface to be able to use Linux with WSL. Here, I will list some
of the most fundamental commands a user should know when starting out.

#### pwd
    
pwd, or print working directory, prints the absolute path of the directory that
you are currently working in. As you become more experience working in a CLI,
you will not use this command so much because you will generally already know
where you are in the filesystem based on the work you are doing. Many users will
even encorporate the path of their working directory into their shell prompt,
rendering the use of pwd redundant. However, when you are first starting out,
this is a useful command when you need to get your barings on where you are in
the system. 

#### ls
    
ls, or list, prints the names of all files in the working directory. This basic
command will remain useful to you for the rest of your life, as it is the
fundamental method of viewing the contents of a directory. 
