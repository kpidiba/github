# CHERRY

## Why Cherry-Pick

Suppose you are working with a team of developers on a medium to large-sized project. Some changes proposed by another team member and you want to apply some of them to your main project, not all. Since managing the changes between several Git branches can become a complex task, and you don't want to merge a whole branch into another branch. You only need to pick one or two specific commits. To pick some changes into your main project branch from other branches is called cherry-picking.

The main motive of a cherry-pick is to apply the changes introduced by some existing commit. A cherry-pick looks at a previous commit in the repository history and update the changes that were part of that last commit to the current working tree. The definition is straight forward, yet it is more complicated when someone tries to cherry-pick a commit, or even cherry-pick from another branch.

Cherry-pick is a useful tool, but always it is not a good option. It can cause duplicate commits and some other scenarios where other merges are preferred instead of cherry-picking. It is a useful tool for a few situations. It is in contrast with different ways such as **merge** and **rebase** command. Merge and rebase can usually apply many commits in another branch.

```git
git cherry-pick <commit id>
```

## Usage of cherry-pick

- It is a handy tool for **team collaboration**.
- It is necessary in case of **bug fixing** because bugs are fixed and tested in the development branch with their commits.
- It is mostly used in **undoing changes and restoring lost commits**.
- You can **avoid useless conflicts** by using git cherry-pick instead of other options.
- It is a useful tool when a full branch merge is not possible due to incompatible versions in the various branches.
- The git cherry-pick is used to access the changes introduced to a sub-branch, without changing the branch.
