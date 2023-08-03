#  Branching and Merging 
- **git branch :**  command lets you create, list, rename, and delete branches ,Each line of development is represented by a branch, and it helps developers to work on features, bug fixes, or experiments without interfering with the main codebase.

### Branch Creation :
- You can create a new branch using the git branch command, followed by the branch name 
- For example, to create a branch named `"jafar-branch"` you would use git branch `jafar-branch`.
 - To create a new branch and switch to it in a single step, you can use git checkout -b `jafar-branch`.
 - You can see the currently active branch by using git branch command with no arguments. The active branch will have an asterisk (*) next to it.
- you can switch between branches using the `git checkout` or `git switch` command followed by the branch name
- When you create or switch to a new branch, all your changes and commits are specific to that branch.
- to Delete the specified merged branch use `git branch -d "branch_name"`
- to Delete the specified unmerged branch use `git branch -D "branch_name"`
- to Rename the current branch to use `git branch -m <branch>`

### Git Checkout (Git switch) :
-  command lets you navigate between the branches created by git branch.
- **Usage :**
    - Existing branches : switch between  branches using git checkout
    - New Branches : command can be used to create a new branch `git checkout -b ＜new-branch＞` method which will create the new branch and immediately switch to it. 

### Detached HEADS : 
- A "detached HEAD" is a term used in Git to describe a specific state where the currently checked-out commit is no longer associated with a branch reference. Instead of being on a branch, your HEAD (which is a pointer to the latest commit of the current branch) points directly to a specific commit. This can happen when you check out a specific commit, tag, or a detached branch.
### Git Merge

