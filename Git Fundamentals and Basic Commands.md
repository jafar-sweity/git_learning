# Git Fundamentals and Basic Commands

## Three Tree Architecture : 
| Component           | Description                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------|
| Working Directory   | The directory where you make changes to your files. These changes can be edits, additions, or deletions.            |
| Index (Staging Area)| An intermediate stage between your working directory and the Git repository. Changes need to be added to the index before committing.|
| Git Repository     | Stores the commit history and the contents of the project. Commits represent snapshots of the project at specific points in time. Each commit points to a tree, which points to the files' content.   |

##  About Git - Git Tutorial for Beginners :
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
