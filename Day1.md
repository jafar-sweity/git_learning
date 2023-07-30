# Introduction to Version Control & Git Basics : 

##  Git Documentation : 
- **What is Version Control ?** 
    - is an important software development practice for tracking and managing changes made to code and other files. It is closely related to source code management.

- **What is Git ?**
    - Git is a distributed version control system (DVCS) and one of the most popular tools used in software development


### Setting up a repository : 
- **git init :**
    - is a command used to initialize a new Git repository in a directory   , it can be used to convert an existing, unversioned project to Git      repository or initialize a new, empty repository. 
    - **Bare repositories --- git init --bare :** is a repository that does not have a working directory , a bare repository only consists of the version control data, including the repository's history, branches, tags, and configuration, but without the checked-out files.
    - The most common use case for  git init --bare is to create a remote central repository:

- **git clone :** 
    - is a Git command line utility which is used to target an existing repository and create a clone, or copy of the target repository.
   
     - **Shallow clone** : it is a lso known as a shallow fetch, is a partial clone of a Git repository where only a limited portion of the commit history is retrieved . 
        - To create a shallow clone, you use the --depth option with the git clone command, or - Shallow since -

##### git clone -mirror vs. git clone -bare :
| Feature                   | `git clone --mirror`                                                                 | `git clone --bare`                                                                  |
|---------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Purpose                   | Creates a mirrored clone of the remote repository.                                  | Creates a lightweight bare clone of the remote repository.                          |
| Version Control Data      | Includes all version control data (commits, branches, tags) and remote references.  | Includes only version control data (commits, branches, tags), no working directory. |
| Working Directory         | No working directory; read-only replica.                                           | No working directory; used for collaboration and hosting.                          |
| Push and Pull Changes     | No; meant for read-only synchronization with the original repository.              | Yes; can be used for collaboration and version control management.                 |
| Additional Information    | Used for backup, migration, and synchronization.                                   | Commonly used as a shared, central repository for collaboration.                   |
| Suitable for Development  | No; read-only nature doesn't allow local development.                               | No; no working directory to directly edit files.                                    |

-  **git config :** command in Git is used to read or modify configuration settings for your Git installation.
    - Git stores configuration options in various files, including system-level, global-level, and local-level configurations.
    - merge tools are external programs or scripts that can be configured to help resolve merge conflicts that occur when Git is unable to automatically merge changes from different branches.
    - color.ui : This is the master variable for Git colors. Setting it to false will disable all Git's colored terminal output.

- **git Aliases** are used to create shorter commands that map to longer commands
- **How do I create Git Aliases?**
     - Directly editing Git config files
     - Using the git config to create aliases


### Getting Started : 
