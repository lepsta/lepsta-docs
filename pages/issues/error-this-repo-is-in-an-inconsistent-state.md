This happens as a result of a validation being performed on a repository. We are working on a fix for this issue.

![Repo in a bad state](/assets/images/repo-in-a-bad-state-3.svg)


!!! note "Note"
    We are working on a fix for this issue. But just in case you come across it before we fix it, please take a look at this guide.



## Why does this happen?
This happens as a result of a validation being performed on a repository. Version control works by creating chained revisions of changes that can reproduce the code you wrote at any point.

Sometimes due to a bug in Uju or the user performing actions that the software is not expecting, this chain of revisions can be broken. This is when a repository is said to be in a bad/inconsistent state. Uju flags the streams that have an issue so that the user is aware of a problem in the relationships of the chained revisions.

Most of the time if a stream is marked as inconsistent, it will stop accepting new changes from any client. We do this to mitigate the risk of corrupting existing changes with the new ones.


## How do I solve it?
We support two ways of fixing this kind of issue. The most appropriate will depend on the effects on branches and streams:

  - **Commit and delete stream**
      If the issue only affects a specific stream, Lepsta will recommend that you commit the changes in that stream (if any) on the web interface as a way to rescue your changes. 
      
      Once you have done this, you can then delete the stream and run `uju update` locally. Once you've done this, you can create a new stream from the web interface and work from there.

  - **Restore the whole repository to an earlier point**
      If the problem is affecting the entire repository, Lepsta will recommend that you restore the repository to an earlier point when it functioned correctly. Please use this as a last resort because it is possible to lose changes from say the past 5 minutes. 
      
      To reduce the effects of this, Uju will backup all local copies of the repository and re-download the new version of the online repository. This means that if you had some changes not committed or replicated, you will not lose them.


We hope that you find this helpful. Please feel free to contact us if you are having any problems.


!!! attention "Attention: Did any of these steps fail?"
    Just in case some of these steps did not go according to documentation, consider making a search on the top bar to check if the issue and solution are documented.