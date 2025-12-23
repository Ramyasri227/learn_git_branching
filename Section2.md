# Git Learning Section2

This documentaion contain the concepts of the Section2 of the Learn Git Branching

# Introduction to HEAD

### **What is HEAD?**

HEAD represents your current position in the Git project history and determines where new commits will be added.

### **What is Detaching Head?**

Detached HEAD means you are directly on a specific commit in your repository's history, rather than on the tip of a named local branch. 

<img width="1920" height="916" alt="Screenshot (110)" src="https://github.com/user-attachments/assets/d58163d8-bddc-46fd-a11a-976dbf876276" />

# Commands Executed

```
git checkout C4
```

The above screenshot illustrates the detached HEAD state in Git using Learn Git Branching.

The commits labeled C0, C1, C2, C3, and C4 represent individual commits in the repository, with the history splitting after C1 into two paths. 

The main branch is pointing to commit C2, while the bugFix branch points to commit C4. 

In this state, HEAD is not attached to any branch but is pointing directly to commit C4. This happens because the command git checkout C4 was executed, which checks out a specific commit instead of a branch.

# Introduction to Relative Reference

### **What is Relative Reference?**

Relative References are a way to refer to commits relative to another reference (like HEAD or a branch name) instead of using full commit hashes. They let you move backward or navigate through the commit history in a simple and readable way.

**Example for Relative Reference(^)**

For example, HEAD^ refers to the immediate parent of the current commit. If a commit has multiple parents (like a merge commit), HEAD^1 refers to the first parent and HEAD^2 refers to the second parent.

<img width="1918" height="912" alt="image" src="https://github.com/user-attachments/assets/93bc53f6-cec6-47ab-b284-9cb404add7da" />

# Commands Excecuted

```
git checkout bugfix^
```

The above screenshot explains the use of relative references in Git using Learn Git Branching.

The commits labeled C0, C1, C2, C3, and C4 represent the project history, where the history splits after C1 into two branches. 

The main branch is pointing to commit C2, and the bugFix branch is pointing to commit C4. In this state, HEAD is moved to commit C3, which is the parent commit of C4.

This is done using the command git checkout C3, demonstrating how Git can move to a commit by referring to its position in history.

The screenshot emphasizes the use of the caret (^) operator, which allows moving to the parent commit of the current commit.

# Introduction to Relative Reference(~)

### **What is Relative Reference(~)?**

Relative Reference (~) in Git is used to move backward through commit history by a specific number of commits.

The tilde ~ moves back multiple commits along the first-parent chain. For instance, HEAD~3 means three commits before the current one.

<img width="1918" height="917" alt="image" src="https://github.com/user-attachments/assets/ebb5cf03-4fea-4a98-984b-3a7709681581" />

# Commands Executed

```
git branch -f main C6
```

```
git checkout HEAD~1
```

```
git branch -f bugfix HEAD~1
```

The above screenshot demonstrates the advanced use of relative references using the tilde (~) operator in Git with Learn Git Branching. 

The commit history shown includes commits C0, C1, C3, C5, and C6 arranged in a straight line, where each commit is built on top of the previous one.

The main branch is currently pointing to commit C6, while the bugFix branch is moved to an earlier commit in the history.

In this level, the goal is to reposition the bugFix branch using relative references from HEAD, rather than checking out commits directly.

The command git branch -f bugFix HEAD~1 is used to forcefully move the bugFix branch to the commit just before the current HEAD position

# Introduction to Revert

### **What is Revert?**

Git revert is a command used to undo the changes of a previous commit by creating a new commit. Instead of deleting or removing the old commit, git revert adds a new commit that reverses the changes made by the specified commit.

<img width="1917" height="912" alt="image" src="https://github.com/user-attachments/assets/ed657bb2-1d31-49ba-885d-f1f60f26d1e5" />

# Commands Executed

```
git branch -f local HEAD~1
```

```
git checkout pushed
```

```
git revert pushed
```

This screenshot demonstrates how changes can be reversed in Git using the revert command in Learn Git Branching.

The commit history shows commits C0, C1, C2, and C2′, where each commit builds on the previous one.

The main (local) branch is pointing to commit C1, while another branch named pushed is currently checked out and points to commit C2, as indicated by the * symbol.

In this scenario, a previous commit on the pushed branch is reversed using the command git revert pushed.

Instead of deleting any commit, Git creates a new commit (C2) that undoes the changes introduced by the earlier commit (C2)
