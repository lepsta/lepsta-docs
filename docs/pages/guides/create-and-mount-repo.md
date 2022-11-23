# Create and mount a Repository

## Introduction
A repository is a data store that keeps track of file metadata and content. It is used by a version control tool to manage changes to files. This guide contains instructions on how to create and mount a repository on the Lepsta platform.

## Concepts
[Learn more about Lepsta repositories](docs/pages/references/concepts/repository.md)
  
## Requirements
  + A Lepsta account;
  + A Github or Bitbucket account. Lepsta allows you to import existing Git repositories. [learn more here](docs/pages/tutorials/integrate_lepsta.md);
  + Basic Knowledge of the command line;
  + Basic knowledge of version control (optional).

## Guide
  1.  Navigate to the `Repositories` tab or navigate to the `+Create` button (top right of the screen) to create a new repository.
  
  ..image placeholder..

  2. A "New repository" page will appear with 3 options for sourcing a new repository, namely: 
  - Brand New - An  empty Lepsta repository
  - Github - Mirror an existing Git repository hosted on github.com
  - Bitbucket - Mirror an existing Git repository hosted on bitbucket.org

    <image placeholder>

  3. Give your repository a name and click on the `Create repository` button.

![Create and mount a new repo](https://static.lepsta.tech/docs-assets/create-and-mount-a-new-repo.gif "create and mount a new repo")


Congratulations on creating your shiny first Lepsta repository. 
Now you have to mount it locally so that you can contribute code to it. 

!!! note "Note"
  Before proceeding to mount your repository, please ensure that you have installed our automatic version control tool, [Uju](docs/pages/guides/install-uju.md).


## Mount a repository
Mounting a repository refers to downloading it to your device so that you can start [contributing code](docs/pages/guides/contribute_code.md). There are 2 ways to do that with Lepsta, using a command or Lepsta desktop app.

* Terminal- run this command on your terminal `uju down workspace_name/repo_name <path>`. Please ensure that you have logged in on the terminal using the same credentials you used on the Platform.

<image placeholder>

* Desktop App - You can also use the Lepsta desktop app to mount the repo. This is the most efficient way to do that. To download the App navigate to the top right of your screen click on "......." and select download.

Once you have downloaded the App, login and search for your repository. Click on `Mount` and your repository will be downloaded.

## Reflection

If you click on `Open` and Visual Studio Code (VS Code) opens, it means you have successfully mounted your repository. To validated further, open a terminal on VS Code and run this command `uju repos`. If your mounted repository appears there, then you're successful.

## Recommended next steps
[How to integrate Lepsta with Github/Bitbucket](pages/tutorials/integrate_lepsta.md)

