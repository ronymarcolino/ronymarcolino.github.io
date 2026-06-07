---
title: "Mastering Git: The Top 5 Useful Commands You Need to Know"
date: 2023-07-08T00:00:00-03:00
draft: false
tags: ["Git", "Software", "Version Control", "Programming"]
categories: ["Development"]
author: "Rony Marcolino"
---

### **Introduction:**

Git has become an indispensable tool for software developers, enabling efficient version control and collaboration. Whether you're a beginner or an experienced developer, understanding and utilizing the right Git commands is crucial for maximizing productivity. In this post, we'll explore the top five useful git commands that every developer should know!

### 1. `git init`

The journey with Git begins by initializing a repository. The `git init` command creates a new Git repository in the current directory. It sets up the necessary Git infrastructure and creates an empty repository for you to start tracking changes. This command is the foundation for version control and allows you to keep track of your project's history.

### 2. `git log --pretty=format:"%h: %x09 %an %x09 %ad %x09 %s"`

If you are investigating the history of commits and need to view them in the form of a list, this command is a great option. With this command you can format the list of commits with hash, author, date and commit message. 

There is also an alternative that offers a summarized form of the date:

```bash
git log --pretty=format:"%h: %s -- %an"
```

### 3. git log --graph
This option in git log presents a visual representation of the commit history, showing the branches and merges in a more intuitive way. This option helps to grasp the project's branching structure and understand the relationships between different branches and commits.

### 4. git config --list
This command in git displays a list of all the repository settings. This is useful for viewing and changing the repository you are working in.

### 5. git fetch --all --prune
The command above is a powerful tool for keeping your local Git repository in sync with the remote repository. When you run git fetch, it retrieves any new commits or branches from the remote repository.

However, if any branches have been deleted on the remote repository since your last fetch, those deleted branches may still exist in your local repository. This is where --prune comes into play. By adding the --prune flag, Git will remove any local branches that no longer exist on the remote repository. This ensures that your local repository accurately reflects the current state of the remote repository, eliminating any outdated or obsolete branches.

git fetch --prune is a handy command for maintaining a clean and up-to-date local Git environment.

### Conclusion:
Mastering the five Git commands discussed above is crucial for developers who want to streamline their workflow, collaborate effectively, and maintain version control. By using these commands, you can initialize repositories, log your commits beautifully, and view your repository configuration.

As you get deeper into Git, you will discover a wealth of other commands and features that can further enhance your development experience. So start with these useful commands, explore Git's capabilities, and unleash its true potential to optimize your software development process.