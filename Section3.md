# Git Learning Guide Section3

This documentation Conatin the concepts of the Learn Git Branching

# Introduction to Cherry-Pick

### **What is Cherry-Pick?**

**Cherry-pick** means choosing one specific commit and adding it to your current branch.Instead of taking all changes from another branch, Git lets you pick only the commit you need and apply it as a new commit. It’s like copy-pasting one change from another branch into your branch.

<img width="1913" height="912" alt="Screenshot 2025-12-23 232908" src="https://github.com/user-attachments/assets/05ea1ce9-67d9-4da8-8cb2-7ef4d4e59ca7" />

# Commands Executed

```
git cherry-pick C3 C4 C7
```

This screenshot demonstrates the use of the git cherry-pick command in Learn Git Branching. 

The commit history begins at C0 and C1, after which multiple branches diverge, including bugFix, side, and another, each containing their own commits such as C3, C5, and C7.

The main branch is currently checked out and marked with main*. In this level, the command git cherry-pick C3 C4 C7 is used to selectively apply specific commits from different branches onto the main branch. 

As a result, new commits labeled C3′, C4′, and C7′ are created on the main branch, preserving the changes from the original commits while maintaining a linear history.

# Introduction to Interactive Rebase

### **What is Interactive Rebase?**

Interactive rebase in Git is a feature that allows you to modify multiple commits before adding them to another branch.It lets you edit, reorder, squash (combine), or delete commits in a commit history. Using interactive rebase, you can clean up your commit history and make it more readable before sharing your work

<img width="1915" height="912" alt="Screenshot 2025-12-23 233257" src="https://github.com/user-attachments/assets/93dc37ea-7793-4d6a-a387-aeaee620e280" />

# Commands Executed

```
git rebase -i HEAD~4
```

This screenshot explains the concept of interactive rebase in Git using Learn Git Branching. 

The commit history starts from C0 and continues through multiple commits, with the main branch currently checked out at commit C4′, as indicated by main*. 

The label overHere points to commit C1, which is used as the base for rebasing. In this level, the command git rebase -i HEAD~4 is used to interactively rebase the last four commits. 

Interactive rebase allows you to reorder, edit, or clean up commits before they are placed onto a new base commit.

