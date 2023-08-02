# Git Fundamentals and Basic Commands

## Three Tree Architecture : 
| Component           | Description                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------|
| Working Directory   | The directory where you make changes to your files. These changes can be edits, additions, or deletions.            |
| Index (Staging Area)| An intermediate stage between your working directory and the Git repository. Changes need to be added to the index before committing.|
| Git Repository     | Stores the commit history and the contents of the project. Commits represent snapshots of the project at specific points in time. Each commit points to a tree, which points to the files' content.   |

##  About Git - Git Tutorial for Beginners :
- [Task Url](https://github.com/eficode-academy/git-katas/tree/master/basic-staging)
- **Recording Changes to the Repository :**
    - when want to start making changes and committing snapshots of those changes into your repository each time the project reaches a state you want to record.
    - Remember that each file in your working directory can be in one of two states:
        - tracked : files that were in the last snapshot, as well as any newly staged files; they can be unmodified, modified, or staged. In short, tracked files are files that Git knows about.
        - untracked : files are everything else — any files in your working directory that were not in your last snapshot and are not in your staging area
- **Checking the Status of Your Files**
    - The main tool you use to determine which files are in which state is the git status command. 
    - Finally, the command tells you which branch you’re on and informs you that it has not diverged from the same branch on the server.
    - `Note "GitHub changed the default branch name from master to main in mid-2020" `

- **Tracking New Files :**
    - In order to begin tracking a new file, you use the command git add. 
- **Staging Modified Files :**
    - Let’s change a file that was already tracked. If you change a previously tracked file called CONTRIBUTING.md and then run your git status command again,
        - The CONTRIBUTING.md file appears under a section named “Changes not staged for commit” — which means that a file that is tracked has been modified in the working directory but not yet staged. 
- **Short Status :**
    - While the git status output is pretty comprehensive, it’s also quite wordy. Git also has a short status flag so you can see your changes in a more compact way. If you run git status -s or git status --short
        - `A` :new files that have been added to the staging area have
        - `M` : modified files 
        - 
- **Ignoring Files :**
    - Often, you’ll have a class of files that you don’t want Git to automatically add or even show you as being untracked. These are generally automatically generated files such as log files or files produced by your build system.
     - **The rules for the patterns you can put in the .gitignore file are as follows :**
        - Blank lines or lines starting with # are ignored.
        - Standard glob patterns work, and will be applied recursively throughout the entire working tree.
        - You can start patterns with a forward slash (/) to avoid recursivity. 
        - You can end patterns with a forward slash (/) to specify a directory.
        - You can negate a pattern by starting it with an exclamation point (!)
- **Viewing Your Staged and Unstaged Changes :**
    - If the git status command is too vague for you — you want to know exactly what you changed, not just which files were changed — you can use the git diff command. 
- **Committing Your Changes :**
    - Now that your staging area is set up the way you want it, you can commit your changes.
    - Alternatively, you can type your commit message inline with the commit command by specifying it after a `-m` flag
- **Removing Files :**
    - To remove a file from Git, you have to remove it from your tracked files (more accurately, remove it from your staging area) and then commit. The git rm command does that, and also removes the file from your working directory so you don’t see it as an untracked file the next time around.


### The Task In Github : 
**Overwrite the content of file.txt with the command echo 2 > file.txt (or sc file.txt '2' in PowerShell)**

1. `git diff` will show the differences between the current state of the file in the working directory and the last committed state in the Git repository.

2. `git diff --staged` (or `git diff --cached`) will show the differences between the current state of the file in the staging area (index) and the last committed state in the Git repository. If this is blank, it means you have not staged any changes yet.

3. Stage your changes from the working directory using the command `git add file.txt`.

4. After staging the changes, running `git diff` will still show the differences between the current state of the file in the working directory (which has not changed since staging) and the last committed state.

5. Running `git diff --staged` will be blank since you have just staged the changes, and the staging area (index) is now in sync with the last commit.

6. Overwrite the content of `file.txt` again with the command `echo 3 > file.txt` (or `sc file.txt '3'` in PowerShell).

7. Running `git diff` will show the differences between the current state of the file in the working directory and the last committed state in the Git repository. It will show the changes made from the content "2" to the content "3".

8. Running `git diff --staged` will still be blank because the changes made in Step 6 are not yet staged.

9. Now, you observed that `file.txt` is present twice in the output of `git status`. This is because you have both the modified (unstaged) version and the changed (staged) version of `file.txt`.

10. To unstage the changes, run `git restore --staged file.txt`.

11. Running `git status` now will show that the changes are no longer staged.

12. Stage the changes again with the command `git add file.txt`.

13. Make a commit with the staged changes using the command `git commit -m "Commit message"`.

14. After the commit, you overwrite the content of `file.txt` with the command `echo 4 > file.txt` (or `sc file.txt '4'` in PowerShell).

15. The content of `file.txt` is now "4".

16. Running `git status` will show that `file.txt` has been modified since the last commit.

17. To discard the changes made in Step 14, you can run `git restore file.txt`.

18. The content of `file.txt` will revert to the state it was in after the previous commit, so it will have the content "2".

19. Running `git status` will show that `file.txt` has been modified, but the changes are not staged. It will also show the changes that were previously staged in Step 12.
