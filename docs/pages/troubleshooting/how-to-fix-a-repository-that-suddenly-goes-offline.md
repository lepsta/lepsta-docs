
# How To Fix A Repository That Suddenly Goes Offline

## Introduction

When a [repository](/pages/references/concepts/repository) suddenly goes offline i.e the repository status indicates it's offline when `uju status` command is run thereby leading to repository changes from local machine not replicating to the Lepsta's repository platform.

## Why It Happened

There're few factors that could be attributed to have been the caused this issue. 
Below is a list of what it could be attributed to
    - **No internet connection**
    An Uju [repository](/pages/references/concepts/repository) is a real-time auto-syncing repository which requires internet connectivity to continously sync and to keep the repository connection status online.

    - **Uju deamon may not be running**

    !!! note A deamon is a computer program that run in the background in a seperate process.

    [Uju](/pages/) after installation will continuously run as deamon(like a background service), which does all the heavy lifting of how Uju and it repositories continously stay connected to ensure continuous replication of user changes. Hence, it is **required** to always have Uju service running.

    - **Replication issue**
    [Replication](/pages/) when replication i.e your changes on your active stream are not showing up in the repository on the Lepsta's platform, this could be as result of either the aforementioned issues above, or more specific issue to the client in question.


## How To Solve It

- **No internet connection** 
Ensure you device is connected to the internet.

- **Uju deamon may not running**
To verify if `Uju` is currently running, any `Uju` issued command when run would return a result with respect to the command. However, will return a very descriptive error. For example, if a user issued Uju command to check on process by running [`uju ps`]() 

`
 Error: 0
 Reason: Could not connect to the server
 Help: Make sure that Uju is running using 'uju service --start'.
`

To resolve this, user needs to run Uju command to bootup Uju service by running `uju service --start`, this command will bootup Uju deamon service.

- **Replication Issue**
When this encountered, there are few options of what to do to allow Uju to "self-heal", as Uju is a very resillient and reliable, this afford it to be able to fix itself.

### Here are the possible options of how to fix it.
    - **Force pushing** the current changes on the active [stream](...), this will prompt Uju to force replication of the active changes on the client's (i.e user's device) to the server.

    - **Repository refresh** this process, makes a quick backup to preserve the current changes on the active stream and redownloads the repository and attach the backed up changes, on the stream back thereby, resuming replication of changes from the stream.

    - **Contact Lepsta Support** Perharps none of the options highlighted above solved the issue for you, when this happens, please contact Lepsta's support [here]() for assistance.

## Reflection 
Was this helpful?



