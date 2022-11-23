# Getting started with Lepsta tutorial

## Introduction 
Lepsta is a real-time collaboration platform for software development teams. It enables teams to improve efficiency in the process of building software.
Lepsta achieves this by providing real-time code synching which opens up a world of benefits such as: 

* Compressed cycle-time
* Team progress visibility
* Reduced feedback-loop

The Lepsta Platform comes with Uju, an automatic version control tool which actively listens to your changes and syncs them to the Lepsta Platform when you click save. To learn more about Uju please [read this document](pages/uju/what-is-uju.md). This document will help you get started.

## Requirements
To get started with Lepsta you only need this:

* A good internet connection;
* A Lepsta account with an email and a strong password;
* A machine running macOS,Linux or Windows operating systems.

That's it, you're ready to use Lepsta.

## Concepts
* [What is a stream]()
* [What is Uju]()

## Tasks

### 1. Create a Lepsta account
To signup you need a valid email address, a strong password and your full name. After you have submitted your details, a confirmation email will be sent and you will be required to click the link to activate your account. You can [create a Lepsta account here](https://app.lepsta.com).

### 2. Setup a team workspace
After signing in into your account you will land on your personal workspace. This workspace is dedicated to your personal projects,it is unshared and only visible to you. If you wish to collaborate with other people you will have to create a ``managed workspace``.

<image placeholder>

A shared workspace allows you to add collaborators, so go ahead and invite your team by email. You can have as many workspaces as you wish and you can easily switch in between them.

### 3. Managed your work
Lepsta was designed to link your task list (known as ``streams`` on Lepsta) with your code. meaning your code changesets will be channeled to your ``stream`` as you work.
Therefore, before you can start coding start by describing what you want to achieve. 

To do that, navigate to the ``Work`` tab and click ``+ New Stream`` and name your stream ``Implement the signup page`` for example. You can also assign it to yourself or to fellow contributors.

### 4. Create a repository
How do you get code to channel to streams? well, you have to attach a repository (repo) to your stream so that the changes you make locally will be synchronized to that particular stream. So let's go ahead and create our repository.

Navigate to the ``Repositories`` tab and click ``+ New Repository``. Now choose one of the 2 ways to create a repo:

1. Create an empty new repo and give it a name or 
2. import an existing repo from Github or Bitbucket - this will import your exiting repo from the selected source and convert it into a Lepsta repo.

!!! note
    When using a repo imported from Bitbucket for instance, all your commits from Lepsta will be replicated and made available to Bitbucket and visa versa. 

### 5. Activate your stream
Navigate back to the ``Work`` tab to view the streams. Pick a stream that you want to work on and attach a repository. Next, click on the status button to see options(see image below). To start a coding task, select ``Start Coding``... 

<image placeholder>

This will open another page and the ``source code and files``  tab will be selected. This is where your code will be displayed when you start working. To start contributing changes, click the button below to activate this stream on your development device. Or you can choose to edit your code online by clicking ``Quick Edit Online`` but for this tutorial we will focus on ``Edit Code Locally``.

<image placeholder>

You will notice that after clicking ``Edit Code Locally`` there will be a notification stating that you have successfully switched and your local repository is now tracking this stream. This means that you have multiple streams and you need to switch to the one you want to work on. Therefore, by clicking that button you are instructing Uju to do the switch for you so that your changes can be channeled to it.

### 6. Download the Lepsta Desktop App
Lepsta's Desktop App is the most efficient way to manage your repositories.To download the App for macOS and Linux machines please use this link [download](installer.dmg) and for Windows OS use this one [download](installer.exe). 

!!! note
    After installing the App on your macOS please ensure that you move it to the application folder. Once you have done that please navigate to the application folder, locate the Lepsta app,  right click and select open as shown below.

<image placeholder>

Login to the app using the same login details you used online. Once you are logged in you will see all the repositories that you are part of.

### 7. Start working (Activation point)
To start working you have to click the ``Mount`` button in order to download your repository. If this has been done successfully, you can click the ``Open`` button which will open Visual Studio code if you have it installed.

Once you have done this you can start coding :),and your changes will be synced automatically to the Lepsta Platform. You will not be required to run any commands to push your code, Lepsta takes care of that.

## Reflection
If you have reached this point you have successfully reached activation. Lepsta's value is mostly realized in a team setting. Go ahead and invite your mates. 
If you encountered issues while trying to get to step number 7, please let us know [here](https://app.lepsta.com/lepsta?collection=11) so that we can help you get started with ease. 

## Recommended next steps
[How to integrate Lepsta with Github/Bitbucket](pages/tutorials/integrate_lepsta.md) 
