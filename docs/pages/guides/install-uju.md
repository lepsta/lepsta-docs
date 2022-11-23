# How to install Uju

## Introduction
Uju is an automatic version control system designed specifically to work with the Lepsta Platform. Instead of running many commands in order to push your code to a code hosting platform, Uju actively listens to your changes and automatically synchronise/push them to the Lepsta Platform as you work.

## Concepts
* [Repository](docs/pages/references/concepts/repository.md)

* [Stream](docs/pages/references/concepts/streams.md)

## Requirements
  + A Lepsta account;
  + A device running either Linux OS, Windows OS or macOS;
  + Basic Knowledge of the command line. 

## Step-by-step Guide

### 1. Install Uju 

#### Linux or MacOs

  Depending on your operating system, you might have `curl` or `wget` pre-installed. You can install Uju by running one of these commands on your terminal.


    ``` 
    curl https://lepsta.tech/get | sh
    ```

    Or

    ```
    wget -qO- https://lepsta.tech/get | sh
    ```


  You can also install the Lepsta desktop app. See image below......



#### Windows

Download the setup file and click on it to install.
        
### 2. Authorising Uju
For you to start working on your Lepsta repositories Uju needs to have access to your Lepsta Platform account. 

* Desktop App - Upon downloading the app. Enter the same credentials you used on the Platform. This will link the desktop app with the Platform.

* Terminal - To authorize Uju on the commandline interface, simply run this command `uju login -u <username>` and your password

![Install Uju](https://static.lepsta.tech/docs-assets/install-to-uju.gif "Install Uju")
 
 ## Reflection
If you have reached this point, you have successfully created a installed Uju. To test this on the commandline interface run this command `uju`. If this is successful you should see a list of Uju commands.

## Recommended next steps
[Working with streams](pages/guides/working-with-streams.md)

