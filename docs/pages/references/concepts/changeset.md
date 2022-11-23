# :octicons-file-diff-24: Changeset

## Introduction
A changeset is a repository object that stores the changes (delta) made to the file. They are similar to commits in terms of their role, but they differ in many aspects:

 - **Lightweight:** changesets only contain enough information to transform the previous version of the file into the new version. Unlike a commit which takes a snapshot of the whole file;
 - **Automatic:** changesets are generated automatically when the user saves changes to a file;
 - **Tracking:** changesets are only tracked by streams and have no working relationship with branches. In short, they are to streams what commits are to branches.

Similarly, to commits, changesets also form a blockchain with each object/block containing the following information:

 - **Timestamp:** when the file was modified/created/deleted or renamed;
 - **Change type:** the type of change being tracked e.g. modify, delete, create or rename;
 - **Content/Patch:** is data that tells Uju how to produce the new version of the file;
 - **User ID:** is the unique identifier of the user that was logged into that Uju instance when the changeset was created.
 - **Previous revision:** to chain the changeset correctly with the ones that precede it.

## Why is it useful?
Changesets are what allows Uju to continuously replicate the changes being made by the user in real-time. You see, commits are too bulky to fulfill this role. As a result, Uju had to introduce this concept of changesets to track them using streams.

When Uju "streams" changes from the stream reference, it is merely just sending changesets and transformation actions across to other replicas to maintain consistency.


## How to use it?
Streams require no effort from the user to be in action. Given that a Lepsta repository always has an active stream, every time that the user makes changes to the files in the repository, a changeset is generated in the background. They are visible by running the command:
```
uju log
```
All the revisions labeled "uncommitted" are actually changesets.


## Related concepts

 - [Commits](/pages/references/concepts/commit) - are produced by generating content from changesets.
 - [Streams](/pages/references/concepts/stream) - store and track changesets to replicate them in real-time.