# :octicons-commit-24: Commit

## Introduction
A commit is a type of repository object that contains a snapshot of the repository labeled with a human-readable message. Commits are an excellent way of packaging changes along with metadata to make it easy to understand what has changed. Inside the commit, the following details can be found:

 - **Message:** a message describing the changes that were made;
 - **Author:** the name and email address of the author;
 - **Committer:** the name and email of the person who generated the commit;
 - **Timestamp:** the time at which the commit was generated;
 - **Stream reference:** the stream reference that acted as the source of changes when a commit was made;
 - **Previous revisions:** one or more revisions that indicate the preceding commit;
 - **Files:** finally the snapshot of files that changed on the commit.

## Why is it useful?
A commit helps us mark a unit of work so that it is possible for branches to track it using revisions. A commit offers the user a chance to describe the work they did in a human-readable fashion. This makes it easy to read the history of the repository.

In addition, commits create the history in the repository because they chain themselves by referencing the previous commits. In the end, you have a blockchain composed of changes that were committed inside the repository.

## How to use it?
Once changes are in a stream, a commit can be generated to snapshot those changes and update the underlying branch to point to the commit's revision. Using Uju, a commit can be generated with the following command (assuming you have made changes).
```
uju commit -m <message>
```
See the relevant guide about how to make and commit changes.

!!! note
    The most convenient way to create commits is by closing a stream on the Lepsta Platform. See the relevant guide for further details.


## Related concepts
Commits affect different parts of the repository, such as:

 - [Branches](/pages/references/concepts/branch) - track commits as part of their history.
 - [Revisions](/pages/references/concepts/revision) - are produced to uniquely identify the commit object.