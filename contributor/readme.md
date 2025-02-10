# CONTRIBUTORS - REMOTE

### GIT FORK

**A fork creates a completely independent copy of Git repository.** **In contrast to a fork, a Git clone creates a linked copy that will continue to synchronize with the target repository**.

**When to Use Git Fork**

Generally, forking a repository allows us to experiment on the project without affecting the original project. Following are the reasons for forking the repository

- Find the GitHub repository which you want to fork.

- Click the Fork button on the upper right side of the repository's page.

- Pull request if you finish

## Fork vs. Clone

Sometimes people considered the fork as clone command because of their property. Both commands are used to create another copy of the repository. But the significant difference is that the fork is used to create a server-side copy, and clone is used to create a local copy of the repository.

There is no particular command for forking the repository; instead, it is a service provided by third-party Git service like GitHub. Comparatively, git clone is a command-line utility that is used to create a local copy of the project.

Generally, people working on the same project clone the repository and the external contributors fork the repository.

A pull request can merge the changes made on the fork repository. We can create a pull request to propose changes to the project. Comparatively, changes made on the cloned repository can be merged by pushing. We can push the changes to our remote repository.



# Contributing to [Project Name]

We are excited to have you contribute to the [Project Name] project! This guide will walk you through the process of making contributions, including how to report issues, create pull requests (PRs), and get involved in the project.

## Table of Contents

- [How to Report an Issue](#how-to-report-an-issue)
- [How to Fork and Clone the Repository](#how-to-fork-and-clone-the-repository)
- [Making Changes](#making-changes)
- [How to Submit a Pull Request](#how-to-submit-a-pull-request)
- [Code Style and Best Practices](#code-style-and-best-practices)
- [Commit Message Guidelines](#commit-message-guidelines)
- [Getting Help](#getting-help)

---

## How to Report an Issue

Before reporting a bug or suggesting a feature, please check the existing issues to see if it has already been addressed.

1. Go to the [Issues](https://github.com/%5Busername%5D/%5Brepo%5D/issues) tab of this repository.
2. Click on **New Issue**.
3. Choose the appropriate issue template (bug report, feature request, etc.).
4. Fill in the required information and be as detailed as possible to help us understand the problem or suggestion.

We appreciate all contributions and feedback!

---

## How to Fork and Clone the Repository

To make changes to the project, you'll need to fork it and clone your fork locally.

1. Fork the repository:
   
   - Go to the project repository on GitHub.
   - Click the **Fork** button in the top right corner.

2. Clone your fork:
   
   `git clone https://github.com/[your-username]/[repo-name].git cd [repo-name]`

---

## Making Changes

1. **Create a new branch**:  
   Always create a new branch for your changes, based on the main branch.
   
   `git checkout -b your-branch-name`

2. **Make your changes**:  
   Update code, fix bugs, or add features as necessary.

3. **Test your changes**:  
   Run any tests to make sure your changes work as expected. Ensure you haven’t broken anything else.

---

## How to Submit a Pull Request

Once you've made changes and committed them to your branch, it’s time to submit a pull request (PR).

1. Push your changes to your fork:
   
   ```bash
    `git push origin your-branch-name`
   ```
   
   Go to the **Pull Requests** tab of the project repository.

2. Click **New Pull Request**.

3. Select your branch from the dropdown and compare it with the `main` branch of the project.

4. Add a descriptive title and description for your PR.

5. Click **Create Pull Request**.

Your pull request will be reviewed by the project maintainers, and they may provide feedback or request changes.



### 1. **Automatically Close Issues with a PR**

When you create a pull request that fixes a specific issue, you can mention the issue in the PR description using keywords like:

```md
Fixes #123
Closes #123
Resolves #123
```

### 2. **Manually Link an Issue to a Pull Request**

If you forgot to mention the issue in the PR description, you can manually link them:

1. Go to the **Pull Request** on GitHub.
2. In the right sidebar, find the "Linked Issues" section.
3. Click **"Link Issue"** and search for the issue number.



---

## Code Style and Best Practices

- Follow the **existing coding style** of the project.
- Keep functions small and focused.
- Avoid unnecessary changes to files you’re not working on.
- Ensure the code is well-commented, especially if the logic is complex.

---

## Commit Message Guidelines

We use [Conventional Commits](https://www.conventionalcommits.org/) for commit messages. Please follow this format:

- **feat**: A new feature
- **fix**: A bug fix
- **docs**: Documentation updates
- **style**: Code style changes (e.g., formatting)
- **refactor**: Code changes that neither fix a bug nor add a feature
- **test**: Adding or modifying tests
- **chore**: Miscellaneous tasks

Example:

```sql
feat: add user authentication module
```

---

## Getting Help

If you need help or have any questions, feel free to open an issue or reach out to the maintainers.
