# CLONE PROJECT

### CLONE WITHOUT AUTHENTIFICATION GITHUB

- **generate token** 

example: 

```git
git clone https://{YOUR_PERSONAL_TOKEN}@github.com/{YOUR_USERNAME}/alx-zero_day.git
```

### CLONE WITHOUT AUTHENTIFICATION GITLAB

```git
git clone https://oauth2:${Personal Access Tokens}@gitlab.com/username/myrepo.git
```

```git
git clone https://gitlab-ci-token:${Personal Access Tokens}@gitlab.com/username/myrepo.git
```

### GIT FETCH

Git "fetch" Downloads commits, objects and refs from another repository. It fetches branches and tags from one or more repositories. It holds repositories along with the objects that are necessary to complete their histories to keep updated remote-tracking branches.

![Git Fetch](https://static.javatpoint.com/tutorial/git/images/git-fetch.png)

**To fetch the remote repository**

```git
git fetch< repository Url>  
```

### To fetch a specific branch

```git
git fetch <branch URL><branch name>  
```

### To fetch all the branches simultaneously

```git
git fetch -all  
```

### Git Fetch vs. Pull

Some of the key differences between both of these commands are as follows:

| git fetch                                                                               | git pull                                                                                        |
| --------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| Fetch downloads only new data from a remote repository.                                 | Pull is used to update your current HEAD branch with the latest changes from the remote server. |
| Fetch is used to get a new view of all the things that happened in a remote repository. | Pull downloads new data and directly integrates it into your current working copy files.        |
| Fetch never manipulates or spoils data.                                                 | Pull downloads the data and integrates it with the current working file.                        |
| It protects your code from merge conflict.                                              | In git pull, there are more chances to create the **merge conflict**.                           |
| It is better to use git fetch command with git merge command on a pulled repository.    | It is not an excellent choice to use git pull if you already pulled any repository.             |

So basically,

```git
git pull = git fetch + git merge
```

### GIT PULL

The term pull is used to receive data from GitHub. It fetches and merges changes from the remote server to your working directory. The **git pull command** is used to pull a repository.

```git
git pull
```



## GITHUB ACCESS PERMISSION SSH

[SSH Keys for GitHub](https://jdblischak.github.io/2014-09-18-chicago/novice/git/05-sshkeys.html#:~:text=Add%20your%20public%20key%20to%20GitHub&text=Login%20to%20github.com%20and,hit%20Add%20key%20to%20save.) 
