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
Git merge conflicts
### Git Checkout (Git switch) :
-  command lets you navigate between the branches created by git branch.
- **Usage :**
    - Existing branches : switch between  branches using git checkout
    - New Branches : command can be used to create a new branch `git checkout -b ＜new-branch＞` method which will create the new branch and immediately switch to it. 

### Detached HEADS : 
- A "detached HEAD" is a term used in Git to describe a specific state where the currently checked-out commit is no longer associated with a branch reference. Instead of being on a branch, your HEAD (which is a pointer to the latest commit of the current branch) points directly to a specific commit. This can happen when you check out a specific commit, tag, or a detached branch.
### Git Merge :
-  is a Git command used to integrate changes from one branch into another. It allows you to combine the work done in different branches and reconcile the differences. 
- git merge is often used in conjunction with git checkout for selecting the current branch and git branch -d for deleting the obsolete target branch.

- **Fast Forward Merge :** A fast-forward merge can occur when there is a linear path from the current branch tip to the target branch.
- **3-way merge :** requires a 3-way merge because main progresses while the feature is in-progress. This is a common scenario for large features or when several developers are working on a project simultaneously.
- merge conflicts will only occur in the event of a 3-way merge. It’s not possible to have conflicting changes in a fast-forward merge. 

### Git merge conflicts : 
- Conflicts generally arise when two people have changed the same lines in a file, or if one developer deleted a file while another developer was modifying it. In these cases, Git cannot automatically determine what is correct
- **How to identify merge conflicts :**  As we have experienced from the proceeding example, Git will produce some descriptive output letting us know that a CONFLICT has occcured. We can gain further insight by running the git status command
 - **When Git encounters a merge conflict, it marks the conflicting sections in the affected files using special conflict markers. These markers help identify the areas of the file where conflicts have occurred and distinguish the conflicting changes from each branch. The conflict markers consist of the following three part** 
 | Conflict Markers     | Explanation                                                                                                                                                                                                                                                                                           |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<<<<<<< HEAD`       | The `<<<<<<< HEAD` marker indicates the beginning of the conflicting section from the current branch (the branch you are currently on, typically the branch you are merging into). Everything between this marker and the `=======` marker represents the changes in your current branch.                |
| `=======`            | The `=======` marker separates the conflicting changes. It acts as a divider between the changes from your current branch and the incoming branch (the branch you are merging from).                                                                                                               |
| `>>>>>>> incoming-branch` | The `>>>>>>> incoming-branch` marker indicates the end of the conflicting section from the incoming branch (the branch you are merging from). Everything between the `=======` marker and this marker represents the changes from the incoming branch.                                                   |

- **Git commands that can help resolve merge conflicts :**
 - git status : The status command is in frequent use when a working with Git and during a merge it will help identify conflicted files.
 - git log --merge : Passing the --merge argument to the git log command will produce a log with a list of commits that conflict between the merging branches.
 - git diff : diff helps find differences between states of a repository/files. This is useful in predicting and preventing merge conflicts.
 - git merge --abort : Executing git merge with the --abort option will exit from the merge process and return the branch to the state before the merge began
