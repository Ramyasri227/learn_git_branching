# Git Learning Branching Section2

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

This screenshot illustrates the detached HEAD state in Git using Learn Git Branching.

The commits labeled C0, C1, C2, C3, and C4 represent individual commits in the repository, with the history splitting after C1 into two paths. 

The main branch is pointing to commit C2, while the bugFix branch points to commit C4. 

In this state, HEAD is not attached to any branch but is pointing directly to commit C4. This happens because the command git checkout C4 was executed, which checks out a specific commit instead of a branch.

# Introduction to Relative Reference

### **What is Relative Reference?**



For example, HEAD^ refers to the immediate parent of the current commit. If a commit has multiple parents (like a merge commit), HEAD^1 refers to the first parent and HEAD^2 refers to the second parent.

<img width="1918" height="912" alt="image" src="https://github.com/user-attachments/assets/93bc53f6-cec6-47ab-b284-9cb404add7da" />

# Commands Excecuted

```
git checkout bugfix^
```

This screenshot explains the use of relative references in Git using Learn Git Branching.

The commits labeled C0, C1, C2, C3, and C4 represent the project history, where the history splits after C1 into two branches. 

The main branch is pointing to commit C2, and the bugFix branch is pointing to commit C4. In this state, HEAD is moved to commit C3, which is the parent commit of C4.

This is done using the command git checkout C3, demonstrating how Git can move to a commit by referring to its position in history.

The screenshot emphasizes the use of the caret (^) operator, which allows moving to the parent commit of the current commit.
