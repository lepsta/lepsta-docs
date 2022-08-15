If you encounter this issue, you need to increase the limits on your operating system to allow Uju to watch files for changes.


![Repo in a bad state](/assets/images/too-many-files-open.svg)


## Why it happens?
You might come across this error when you try to download a repository. This happens because Uju needs to watch your project for changes. To do this, it subscribes to file events emitted by the operating system. Usually, there are limits to how many files can be watched at the same time. And a lot of programs might rely on this feature.


## How to solve it?
You would need to increase these limits on your development machine to work around this. Different operating systems have different settings to adjust this.

=== "Linux"
    In most Linux distributions, you can update these limits by updating the ``fs.file-max`` variable in ``/etc/sysctl.conf``. Once you've done this, you can run:

    ```
    # sysctl -p
    ```

    to persist the changes system-wide.


=== "MacOS"
    To increase the limit on MacOS, you can run the following command:

    ```# sysctl -w kern.maxfiles=value
    ```

    value is a new, higher limit that you want to set.


=== "Windows"

    !!! Danger "Windows version  is not available yet"
        We are still working on the Windows version and will make an announcement as soon as it is available.


!!! Note 
    There is no "correct" number to use for this limit. You can set it as high as possible given the specifications of your computer.



!!! attention "Attention: Did any of these steps fail?"
    Just in case some of these steps did not go according to documentation, consider making a search on the top bar to check if the issue and solution are documented.