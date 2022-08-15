# Lepsta Docs

This repository contains documentation for the Lepsta Platform and Uju.

## Installation

To pull the code down from Lepsta, run the command:
```
uju down lepsta/docs <path>
```

## Setup

This documentation website is build using Mkdocs. For complete documentation, see [https://squidfunk.github.io/mkdocs-material/getting-started/](https://squidfunk.github.io/mkdocs-material/getting-started/).

## TL;DR

Make sure you have Python installed and simply run:
```
pip3 install mkdocs-material
```
Once installed, you can run the website using:
```
mkdocs serve
```
The site will run on `http://120.0.0.1:8000`.

## INSTALLATION ON MAC
To run..
Run `python3 -m mkdocs serve`

Installating on Mac and still facing challenges, visit this iste for help;
[https://suedbroecker.net/2021/01/25/how-to-install-mkdocs-on-mac-and-setup-the-integration-to-github-pages/]


## Running in Docker
This is the easiest and probably most convenient way to run this projects. To use Docker, you first need to install it. You can follow these guides to do this: [https://docs.docker.com/engine/install/](https://docs.docker.com/engine/install/).


Once Docker is running, you need to add the Docker run command as an alias. You only need to run the following steps once. After that, you will simply use `run-mkdocs` to run the project. 

> **INFO:** An alias is like a shortcut command so that you do not have to remember the long version of the command.

To do this, run the following command:

```
echo "alias run-mkdocs='docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material'" >> ~/.bash_aliases
```

To make sure that the alias is loaded, you can simply run the following command once:

```
source ~/.bash_aliases
```

From then on, you will be able to run mkdocs with `run-mkdocs` (first run may be slow since it will pull down the docker image).


> **IMPORTANT:** You need to run `run-mkdocs` from inside your repository folder, otherwise you will get this error: `Config file '/docs/mkdocs.yml' does not exist.`.