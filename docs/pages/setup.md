**I think we should exclude this as its covered on the tutorial**


# Setup
This guide will walk you through how to setup a Lepsta account which you will use to import or create repositories and to collaborate with others.

To start using Lepsta, you need two things.

 - An account on the [Lepsta Platform](https://lepsta.tech/auth/signup).
 - A Linux or macOS computer running Uju (our automatic version control tool).
 - Note for users who have Windows OS. There is a firewall issue that we are currently battling with. As a temporary solution kindly install a VM to run Linux.


## Create a Lepsta Platform account
To create a new account, <a href="https://app.lepsta.com/auth/signup" target="_blank">click here</a>. All you will need is your own email address, and a strong password.
Alternatively, Lepsta lets you setup your account using third party authentication providers like Google, GitHub and Bitbucket.

To ensure that you have captured your details correctly, you will be asked to verify your email address after signing up for a new account. Please check your email, also check your spam box if it doesnt appear on your primary inbox.

!!! note "Note"
    Authorising your development computers to access your Lepsta Platform account still requires that you set up a password. So, even if you sign up with an OAuth service provider, you will be asked to set up a password, even though this might change in the future.


## Initial setup
Please note, if you are a non-techincal person and you wont be writing coding using Lepsta, you can ignore the instructions below, however, you can still use Lepsta to manage yours and other people's tasks. Please see more [here](/pages/guides/create-a-workspace). If your code, keep reading.


!!! information "What is Uju"
Uju is a version control server designed specifically to work with the Lepsta Platform. You need to have it installed to contribute to your repositories and to collaborate with others.

### System Requirements
 - Linux or Mac operating system. (**Recommended**) 
 - Windows operating system. 

  Now that we understand what Uju is and what requirements we need,you can go ahead and click on ``add a different device`` to proceed.

### Installation instructions

#### Linux or MacOs

Depending on your operating system, you might have `curl` or `wget` preinstalled.
You can install Uju by running one of these commands on your terminal.


``` title="Install Uju"
curl https://lepsta.tech/get | sh
```

Or

```
wget -qO- https://lepsta.tech/get | sh
```


#### Windows

We have a new windows version.

## Download Uju Locally
For you to start working on your Lepsta repositories Uju needs to have access to your Lepsta Platform account. To authorize Uju, you need to login from the commandline interface. Simply run the following command, and you are good to go:

```
uju login -u <username>
```
OR 

Enter your username after promted by uju;

![Login from Uju on your command line!](/assets/images/login-to-uju.gif "Login from Uju")


!!! attention "Attention: Did any of these steps fail?"
    Just in case some of these steps did not go according to documentation, consider making a search on the top bar to check if the issue and solution are documented. :smile: