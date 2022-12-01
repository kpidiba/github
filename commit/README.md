# COMMITS

Commits can be thought of as snapshots or milestones in the timeline of a Git project. They are created using the git commit command to capture the state of a project at a point in time.

- **git add** :  adds a change in the working directory to the staging area.

```git
git add .
git add <file>
git add <directory>
```

- **git commit** : captures a snapshot of the project's currently staged changes. Committed snapshots can be thought of as “safe” versions of a project—Git will never change them unless you explicitly ask it to. Prior to the execution of `git commit`, The `git add` command is used to promote or 'stage' changes to the project that will be stored in a commit. These two commands `git commit` and `git add` are two of the most frequently used.

```git
git commit -m "Message" 
git commit (open an editor add the message at the top)
 git commit -a  (It is used to commit the snapshots of all changes.
 This option only consider already added files in Git.
 It will not commit the newly created file)
```

- **git log** : is a utility tool to review and read a history of everything that happens to a repository. Multiple options can be used with a git log to make history more specific,generally, the git log is a record of commits.

**The above command will display the last commits. Consider the below output**

```git
git log
```

**So, usually we can say that the --oneline flag causes git log to display**

```git
git log --oneline
```

**The above command will display the files that have been modified**

```git
 git log --stat
```

**The git log patch command displays the files that have been modified. It also shows the location of the added, removed, and updated lines**

```git
git log --patch  
```

## Filtering the Commit History

**By Amount:**

```git
git log -n 3
```

**By Date and Time:**

```git
 git log --after="yy-mm-dd"
 git log --after="2019-11-01" --before="2019-11-08 "  
 git log --after="21 days ago"
```

**By Author:**

```git
git log --author="Author name"  
```

### Modify Commit

```git
git commit --amend
git push --force
```
