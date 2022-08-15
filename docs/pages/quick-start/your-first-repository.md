!!! info "Is your setup running?"
    You must have gone through setup to create your first repository.

### Create a workspace
You can either create a team workspace or use your personal workspace which is created by default. To learn more about creating workspace check this [guide](/pages/guides/create-a-workspace).

## Create your first repository
To create your first repository, you need to set it up from the <a href="https://app.lepsta.com/a/new-repo" target="_blank">Lepsta Platform</a>. Lepsta allows you to either create a brand new repository, or Import (link) an existing Git repository.

=== "Brand new repo"
    If you chose this option, your repository will be created on the Lepsta Platform, and will not be linked with an existing repository.

=== "Import from GitHub"
    This option will allow you to create a repository as a mirror of an existing Git repository hosted on Github. This means that the two repositories will become linked and changes will be synced between the two of them.

=== "Import from Bitbucket"
    This option will allow you to create a repository as a mirror of an existing Git repository hosted on Bitbucket. This means that the two repositories will become linked and changes will be synced between the two of them.

![Create a new repository on the Lepsta Platform](/assets/images/new-repo-screen.png)

## Download (Mount) your first repository
After creating your repository on the platform, you can use Uju to mount it on your development computer so that you can start contributing changes to it. To do this, you can run the following command:

```
uju down <yourusername>/<reponame> <localpath>
```

!!! tip "Tip"
    You can get the "correct" command from the platform after creating your repository. See the example below:

![](/assets/images/create-and-mount-a-new-repo.gif)

Once the repository is available on your development computer, you can open it using a code editor of your choice and start working.

!!! attention "Attention: Did any of these steps fail?"
    Just in case some of these steps did not go according to documentation, consider making a search on the top bar to check if the issue and solution are documented.