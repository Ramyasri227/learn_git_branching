
# Git Learning Guide

This contains learning notes for Git, created to understand how Git works internally using concepts explained through Learn Git Branching.

# Learn Git Branching

Learn Git Branching is an interactive, browser-based learning platform that helps users understand how Git works internally through real-time visual diagrams, covering concepts such as commits, branches, HEAD, merging, and rebasing.

# What it does

Simulates a Git repository in a safe environment

Visually shows commits as nodes and branches as pointers

Updates the commit graph in real time when Git commands are executed

# Concept it teaches:

Creating and understanding commits

Working with branches and HEAD

Switching branches using checkout / switch

Merging branches and resolving conflicts 

Rebasing and understanding linear vs non-linear history

Detached HEAD state

# Why it is effective

Converts theoretical Git concepts into visual understanding

Helps learners see the exact effect of each command

Reduces fear of breaking real repositories

Ideal for beginners as well as intermediate learners

# Introduction to Git Commits

### **What is Git Commit?**

A **Git commit** is a record that saves the current state of a project in a Git repository. It stores the changes made to files along with a message describing those changes, allowing Git to track the project’s history over time.


<img width="1920" height="910" alt="image" src="https://github.com/user-attachments/assets/2d683427-b061-44ce-9326-3aacdcd92029" />

# Commands Executed
```bash
git commit
git commit
```
This screenshot shows how commits are created in Git.

Each circle (C0, C1, C2, C3) represents a commit made one after another.

The (main*) label shows the current branch, and it points to the latest commit (C3).

Every time git commit is used, a new commit is added and the main branch moves forward.

This helps us understand how Git keeps track of changes.

# Introduction to Git Branching

### **What is Git Branch?**

A branch in Git is like a separate workspace for your code. It allows you to work on new features or fixes without affecting the main code

### **What is Git Chechout?**

The git checkout command is used to switch between these branches, so your files and code update to match the branch you select.

<img width="1920" height="922" alt="Screenshot (108)" src="https://github.com/user-attachments/assets/04c430a4-adbb-4286-b449-1764e8f36bab" />

# Commands Executed
```bash
git branch bugfix
git checkout bugfix
```

This screenshot shows how to create and switch to a new branch in Git using Learn Git Branching.

The commits C0 and C1 are displayed, with C1 being the latest commit.

A new branch named bugfix has been created from commit C1 using git branch bugfix, and it has been checked out using git checkout bugfix.

The * symbol next to bugfix indicates that HEAD is currently on this branch.

The main branch still points to commit C1, but the active branch is now bugfix.

# Inroduction to Git Merging

### **What is Git Merging?**

Git merging is the act of combining changes from one branch into another branch so that both branches work exists together in a single branch.

<img width="1920" height="923" alt="Screenshot (106)" src="https://github.com/user-attachments/assets/b54d20c5-d13d-4e77-bd1f-698053f75965" />

# Commands Executed
```bash
git branch bugfix
git checkout bugfix
git commit
git checkout main
git commit
git merge bugfix
```

This screenshot illustrates the Merging in Git level from Learn Git Branching, showing how Git manages multiple branches and combines them. 

The circles labeled C0, C1, C2, C3, and C4 represent individual commits, with the history first moving linearly from C0 to C1 and then splitting into two paths. 

From commit C1, a new branch named bugfix is created and points to commit C2, while the main branch continues independently with commits C3 and C4. 

The label main* indicates that the main branch is currently checked out, with the * symbol showing that HEAD is pointing to main at commit C4. 

The curved lines in the diagram visually represent the divergence of the two branches and their integration through a merge.

# Introduction to Rebase

### **What is Git Rebase**

Git rebase is the process of moving or replaying commits from one branch onto another branch, changing the base commit so the history becomes linear.

<img width="1920" height="921" alt="Screenshot (109)" src="https://github.com/user-attachments/assets/aede8db6-62ef-4e5b-9442-41b846379451" />

# Commands Executed
```bash
git branch bugfix
git checkout bugfix
git commit
git checkout main
git commit
git checkout bugfix
git rebase main
```

This screenshot shows the Rebase Introduction level in Learn Git Branching, illustrating how rebasing works in Git. 

The commit history begins linearly from C0 to C1, after which it splits into two branches. 

The main branch points to commit C3, while the bugfix* branch is currently checked out and points to C2, as indicated by the * symbol showing that HEAD is on the bugfix branch. 

The diagram shows that the bugfix commit has been moved and reapplied on top of the latest commit of the main branch, resulting in a straight, linear history. 

The renaming of the commit to C2′ visually represents that the commit was recreated during the rebase process.
