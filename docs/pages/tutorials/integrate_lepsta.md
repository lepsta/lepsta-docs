# Using Lepsta with your Git repositories

## Introductions
Lepsta plays well with other tools, it was built to supercharge your workflow and productivity, not to replace your existing setups. Migrating your existing repositories (repos) was made easier for your convenience. 

This document demonstrates how to Integrate Lepsta with Bitbucket and Github to enable teams to gradually adopt Lepsta without losing pipelines, tests, deployments, automation etc that are already set up.

## Requirements
You will only need this:

* A Lepsta account;
* A Github or Bitbucket account.

Also, you are quired to grant Lepsta access to the third-party tool to complete the integration.

!!! Note
    This tutorial assumes you have existing repositories sitting on Github or Bitbucket

## Concepts
[Commits]()

## Tasks 

## 1. login to your Lepsta account
If you have not created your Lepsta account yet please  complete the [How to get started with Lepsta tutoria](pages/tutorials/get_started.md) first. Once you have logged in, you may proceed to the second step:

## 2. Integrate Lepsta
``Integrating`` in this case means mirroring your Github/Bitbucket repository such that Lepsta commits reflect on Github and visa versa. 

To do that, navigate to the ``+ Create`` button on the top right of you screen. Click and select ``A repository``.

<image placeholder>

There are three options there,to import an existing repo select your hosting provider e.g Github. A message will be shown stating that Github is not yet connected. Click on ``Connect`` to grant Lepsta access to your Github account.

You will be prompted to enter your Github login details to complete the integration. Follow that process until Lepsta is fully authorized and you will be redirected back to Lepsta. If this was successful, you can move to the next step

## 3. Import your Github/Bitbuckt repo
Now the code hosting provide that you connected and a drop drop-down list of your repositories from your selected hosting provider will appear. Select the one you want to contribute to and give it a name. Click the ``Mirror repository`` button and it will be converted into a Lepsta repository. 

## 4. Mount your repo and start coding
You have successfully integrated Lepsta. The next thing to do is to mount/download your repo locally and start coding. The [How to get started with Lepsta tutoria](pages/tutorials/get_started.md) covers that process in more detail. After mounting your repo you can start coding, drink your coffee and watch the magic happen.

## 5. What gets mirrored?
You will notice that once you start coding your changesets get synchronized (automatic push) to lepsta.com, but these changesets don't get mirrored to Github Immediately until you commit your changes. When you are happy with your progress you may run this commit command ``uju commit -m 'commit message'".

Lepsta commits trigger a push to Github/Bitbucket. Similarly, when someone else in your team commits their code to Github/Bitbucket using Git, their commits will also reflect on Lepsta.


<image placeholder>


## Reflection
Did your commit reflect on Github/Bitbucket? Great! it means you have successfully integrated Lepsta. Happy coding. 

## Recommended next steps
We list any related tutorials that we think the reader could be interested in
