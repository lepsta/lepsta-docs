# :octicons-diamond-24: Revision

## Introduction
A revision (sometimes referred to as an Object ID) is an immutable unique identifier of objects within the repository. Revisions are produced when new versions of files are created. This can be as a result of a commit being made, or a changeset being created. Revisions are created using a hashing algorithm that produces digests that have a very low probability of colliding. A sample revision generated using the MD5 hashing algorithm looks something like this:
```
f7b85d0cf32e50fbd2c658f04687f339
```

!!! note
    There are different types of hashing algorithms that can be used to generate revisions. For example, [MD5](https://en.wikipedia.org/wiki/MD5), [SHA-1](https://en.wikipedia.org/wiki/SHA-1), [SHA-256](https://en.wikipedia.org/wiki/SHA-2) and more.


## Why is it useful?
Revisions are very important in helping us reliably identify a specific version within a repository. While it could be easier to say for instance "revert to yesterday at 4 pm", there is a possibility that another event occurred at that time from another user. Therefore, to prevent ambiguity, revisions would look different even if they were created at the same instance.

## How to use it?
Revisions have many uses. Uju itself is always using revisions to keep track of changes and which versions of files it's currently pointing to. You can also use revisions in the following scenarios:

 - **Comparison:** to compare two different points in the repository history;
 - **Resetting:** to revert to a previous version within a stream or branch;
 - **Hyperlinking:** to create permanent links to a particular object.

Any object that is stored in the database has a revision associated with it. The most used revisions however are those that point to a [commit](/pages/references/concepts/commit) or a [changeset](/pages/references/concepts/changeset).

## Related concepts

 - [commit](/pages/references/concepts/commit)
 - [changeset](/pages/references/concepts/changeset)