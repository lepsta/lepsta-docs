# How to install Uju

## Introduction
This guide contains instruction outlined to successfully install Uju on your local machine.


## Outline of the objective of the article

!!! Abstract "What is Uju"
  Uju is a version control server designed specifically to work with the Lepsta Platform. You need to have it installed to contribute to your repositories and to collaborate with Lepsta platform.

## Requirements
  + A Lepsta account.
  + Linux or Mac operating system. (Recommended)
  + Windows operating system.
  + Basic Knowledge of the command line.

Now that we understand what Uju is and what requirements we need, you can go ahead and click on add a device to proceed.
 

## Brief definition of important concepts (linking them to the reference section)
[Repository](docs/pages/references/concepts/repository.md).
[Stream](docs/pages/references/concepts/streams.md).
[Uju] (docs/pages/references/concepts/uju.md)
 

## Guide (step-by-step)
### Installation instructions
### Linux or MacOs

  Depending on your operating system, you might have `curl` or `wget` preinstalled.
  You can install Uju by running one of these commands on your terminal.


    ``` title="Install Uju"
    curl https://lepsta.tech/get | sh
    ```

    Or

    ```
    wget -qO- https://lepsta.tech/get | sh
    ```

  You can also install the Lepsta desktop app. See image below......



#### Windows

Download the setup file and click on it to install.
        

For you to start working on your Lepsta repositories Uju needs to have access to your Lepsta Platform account. 
To authorize Uju, you need to login from the commandline interface. Simply run the following command, and you are good to go:

```
uju login -u <username>
```
OR 

Enter your username after promted by uju;


 
If you have reached this point, you have successfully created a new repository. 
If that is not the case, see …. For troubleshooting


## Recommended next steps
Working with streams

