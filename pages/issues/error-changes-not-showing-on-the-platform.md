Errors on Uju may cause your changes to not get picked up or replicated. Follow these steps to resolve this.

![Changes not replicating](/assets/images/changes-not-showing-1.svg)

## Why it happens?
The most likely cause of this is Uju or the repository itself not running. Uju is only able to index and replicate your changes if it remains running and is able to watch the files in your project.
Another possibility could be that you are not connected and Uju is not able to replicate changes. This can be caused by various factors such as network configuration (among others).

## How to solve it?
To find the best solution, we need to first establish what is really causing the error.

### Is Uju running?
One of the things to check is if Uju is running. To do that, ``run uju repos``. If you see the following error, it means that Uju is not running:

```
 Error: 0
 Reason: Could not connect to the server
 Help: Make sure that the System daemon is running.
```
 
### Is the repository running?
If you've ascertained that Uju is running, you may want to confirm that the repository is also running and connected. Using the ``uju repos`` command again, check the status of your repository. You should see output like this:

```
ID            NAME        PATH                MODE   RUNNING   ONLINE
088936c6f143  bbd-todo   /Users/david/todo   client  ● yes     ● no
86ea24f43eb5  demo       /Users/david/demo   client  ● yes     ● yes
```



### Anything in the logs?
If your repository run or online status is ``● no``, you can check the logs to see if there are errors indicating why it is not running or online. Uju logs are found in ``~/.uju/uju.log`` in Unix operating systems and in ``C:\Users\<username>\AppData\Local\Packages\uju\uju.log``.


Most issues can be resolved by simply restart Uju using the command ``uju system -s``. But it's good to know what the issues is to prevent loss of data and or report it.

!!! attention "Attention: Did any of these steps fail?"
    Just in case some of these steps did not go according to documentation, consider making a search on the top bar to check if the issue and solution are documented.