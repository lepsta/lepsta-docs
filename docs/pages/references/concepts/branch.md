# :octicons-git-branch-24: Branch

## Introduction
A branch is a type of [repository](/pages/references/concepts/repository) reference that marks a particular point in history. It's like a bookmark that marks a point where a unique snapshot of the repository can be computed. When this happens, it can produce the files as they were at that particular point in time. 

## Why is it useful?
Since repositories are configured to allow contributions from different people, branches can come in handy. This is because they can help fulfill the following purposes:

 - **Implementing workflows:** branches can be used to maintain different copies of the same code base for example. At any point, the contents of the branch can be merged into other branches to create new copies of the code base. This makes it possible to create sophisticated workflows.

 - **Isolating work:** branches can be used to give every contributor an isolated sandbox through which they can make contributions. This is important because it allows everyone to work without interruptions. When they are ready, their branch can then be merged into other branches once the work is accepted.

There is a lot more that can be achieved using branches because they are versatile and lightweight.

## How to use it?
Branches are created inside a repository using the [Uju](/pages/uju/what-is-uju) version control tool. This can be done through multiple interfaces, but ultimately a reference gets created where file changes can be committed. Branches are created based on a revision, which is an address that marks a particular point in history.

Using Uju, a branch (`develop` for example) can be created with:

```
uju branch develop
```

This will generate a reference pointing to the active revision of the repository. Any user can view and contribute to any branch. To contribute changes to a branch on Lepsta, [commits](/pages/references/concepts/commit) are used.

To switch between branches on a Lepsta repository, the following command can be used:

```
uju switch main
```
Where `main` is the name of the destination branch.

## Related concepts
Branches only work because of commit revisions. See the following sections for more information:

 - [Commit](/pages/references/concepts/commit)
 - [Revision](/pages/references/concepts/revision)