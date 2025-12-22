# Learn Git Branching

# Introduction to Head

### **What is Head?**
HEAD is a reference to the current check-out commit in your repository. It's basically a pointer or symbolic reference to the latest commit in your branch.

### **What is Detaching Head?**
Detaching HEAD in Git means that HEAD is pointing directly to a specific commit instead of a branch.

<img width="1920" height="916" alt="Screenshot (110)" src="https://github.com/user-attachments/assets/0d2d694f-277d-4b75-b878-01a0a3d59504" />

This screenshot illustrates the detached HEAD state in Git using Learn Git Branching. 

The commits labeled C0, C1, C2, C3, and C4 represent individual commits in the repository, with the history splitting after C1 into two paths.

The main branch is pointing to commit C2, while the bugFix branch points to commit C4. In this state, HEAD is not attached to any branch but is pointing directly to commit C4.

This happens because the command git checkout C4 was executed, which checks out a specific commit instead of a branch.

When HEAD is detached, you can view or test the project at that commit, but any new commits created in this state will not move any branch unless you switch to or create a branch
