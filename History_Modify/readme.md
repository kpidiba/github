# HISTORY MODIFY

### Go back as a spectator (commits made will not be taken into account when going back when you are a spectator)

```git
git log --oneline (to see what level I want to return to)
git checkout (the hexadecimal number displayed before the name of the commit)
```

### Return to initial state

```git
git checkout nomdelabranche
```

### Retrieve the contents of the file at this commit

```git
git checkout (nombre hexa) nomdufichier
```

### Undo a commit, undo anything done during a commit

```git
git revert (nombre hexa )
```

### To undo the undo just undo the commit that undoes the other commit

### revert to last commit perform

```git
git reset --hard
```

### go back to a commit by undoing the other commits that follow it

```git
git reset (nombre hexadecimal du commit)
```
