# :octicons-zap-24: Stream

## Introduction
A stream is a replicated sandbox that can contain file changes and other related information. Just like a branch, a stream in the repository is represented as a reference that points at a specific revision in the repository. However, unlike a branch, streams are designed to automatically track and *stream* changes in real-time across all repository replicas. As a result, stream track [changesets](/pages/references/concepts/changeset) instead of [commits](/pages/references/concepts/commit).

A stream reference is tied to a specific branch and cannot be moved. Changes inside a stream can be copied to other streams via the `uju import` command, or persisted to a branch via the `uju commit` command. 

!!! important
    On Lepsta repositories, commits are produced from stream references. This means that to make a commit to the underlying branch, those changes must have been on the stream before.


## Why is it useful?
The primary goal for streams is to make contributions portable with ZERO effort from the contributor. To achieve this, streams work like a replicated state machine. Meaning that what is on machine A is the same (eventually consistent) as what is on machine B. This unlocks a lot of posibilities that are just not possible with branches. For example:

 - **Redundancy:** same changes live in different machines, which means they are safe at all times;
 - **Visibility:** all contributions are visible as they develop, which makes it possible to perform incremental checks;
 - **Clean working copy:** there is never a need to stash changes before switching;
 - **Microversions:** you can reset through uncommitted changes. For example going back to the state you had 10 minutes ago;
 - **Access control:** streams are by default assigned to the user that created them. While others can (by default) see the contents, this can be changed.

All of this without bloating the repository with commits like "small change" or "changed stuff" just for the sake of making a put.

!!! important
    Streams on the Lepsta Platform are a high level abstraction over the repository stream references. They are an application or solution that is powered by the Uju stream references.

## How to use it?
Lepsta repositories ALWAYS have a stream active, and this happens automatically. For example, if you mount a Lepsta repository on your local machine, it will automatically create a stream reference using your username. To confirm this, simply run the following command on any repository.
```
uju stream
```
This will print out a list of stream references on the current branch. Stream references also get created automatically when you `uju switch` to a branch.

!!! tip "Tip: For better experience, manage streams on the Platform"
    While this is useful for quick changes, for the best experience, use the Lepsta Platform to create streams if you want to collaborate with other people.

For more information on how to use streams, see the relevant guide.


## Related concepts
Streams are only able to track changes using changesets. During normal operation, they are indexing file changes as changesets and then when a commit is made, changes are moved into a commit object. During the commit operation, the underlying branch will be updated to include such a commit. See the following for more details:

 - [Branches](/pages/references/concepts/branch)
 - [Changesets](/pages/references/concepts/changeset)
 - [Commits](/pages/references/concepts/commit)