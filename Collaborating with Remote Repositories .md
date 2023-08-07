#   Collaborating with Remote Repositories - GitHub 

## Working with remote in git  
- Working with remotes in Git involves collaborating with others and synchronizing your local repository with remote repositories hosted on Git hosting services (e.g., GitHub, GitLab, Bitbucket) or other remote servers in local 
- **Adding a Remote :** Use git remote add command to add a remote repository to your local repository. The remote name is typically "origin," but you can use any name you prefer ` git remote add origin <remote-url> or path if it in local `
- **Fetching Changes :** Use git fetch to retrieve changes from the remote repository without merging them into your local branch but the changes will not be merging 
- **Pulling Changes :** Use git pull to fetch and merge changes from the remote repository into your local branch in one step.
- **Pushing Changes :** Use git push to push your local changes to the remote repository. 
- **Cloning a Remote Repository :** Use git clone to create a copy of a remote repository on your local machine. 
- **Pull Requests (GitHub, GitLab, etc.) :** Many Git hosting services provide pull request functionality. A pull request allows you to propose changes to a repository and request that the changes be merged into the main branch.


## GitHub 
- GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.
- GitHub hosts Git repositories, allowing developers to store and manage their code in a centralized location. Users can create both public and private repositories for individual projects or team collaborations.

- **Creating a branch :** Branching lets you have different versions of a repository at one time , By default, your repository has one branch named main that is considered to be the definitive branch
- **Making and committing changes :**  When you created a new branch in the previous step, GitHub brought you to the code page for your new readme-edits branch, which is a copy of main 
    - You can make and save changes to the files in your repository. On GitHub, saved changes are called commits. Each commit has an associated commit message, which is a description explaining why a particular change was made. 

- **Opening a pull request :** Pull requests are the heart of collaboration on GitHub. When you open a pull request, you're proposing your changes and requesting that someone review and pull in your contribution and merge them into their branch. Pull requests show diffs, or differences, of the content from both branches. The changes, additions, and subtractions are shown in different colors.
    - **Merging your pull request :**   Sometimes, a pull request may introduce changes to code that conflict with the existing code on main. If there are any conflicts, GitHub will alert you about the conflicting code and prevent merging until the conflicts are resolved.
