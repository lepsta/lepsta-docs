# Create and Mount a Repository

### Introduction
This guide contains instruction outlined to successfully create a repository on the lepsta platform.

### Outline of the objective of the article
  
### Requirements
  + A Lepsta account.
  + A Github or Bitbucket account.
  + Basic Knowledge of the command line
  + Basic knowledge of version control (optional).

### Brief definition of important concepts
[Repository](docs/pages/references/concepts/repository.md).

### Guide
  - Navigate to the``Repositories`` tab to create a new repository.
  - Select the source of the Repository
    - Brand New - A brand new Lepsta repository
    - Github - Mirror an exising Git repository hosted on github.com
    - Bitbucket - Mirror an existing Git repository hosted on bitbucket.org

 - **Brand New Repository**
    - Give your repository a name and click on the `create repository button`.
    
     To learn more about importing a repo, see this article [How to integrate Lepsta with Github/Bitbucket](pages/tutorials/integrate_lepsta.md) "

Congratulations on creating your shiny first Lepsta repository. 
Now you have to mount it locally so that you can contribute code to it. 

In order to do that however, you must install Uju to your machine first.
Follow this link to see how to install Uju.....


### Mount a repository

``` title="Steps to mounting a repository"
    
    - Select the device you want to mount to
    - You can use the wizard or use the terminal
    - Copy the command below and run it on the terminal. 
    Be sure to replace the <path> with your folder path.
    ```
    $ uju down lepsta/lepsta <path>
    ```
    - `Cd` into your repository


If you have reached this point, you have successfully created a new repository. 
If that is not the case, see …. For troubleshooting


###  Recommended next steps

+ Working with streams....
+ Create a team workspace
