#   GitHub Workflow and Project Management

## Git Flow 
- it is a branching model and workflow for software development that provides a structured approach to managing branches and releases in Git repositories. 
-  **Main Branches :** 
    - master : The main branch represents the production-ready code
    - develop : The develop branch serves as an integration branch for ongoing development
- **Supporting Branches :** 
    - feature : Feature branches are created for developing new features or enhancements.
    - release : Release branches are created when preparing for a new release
    - hotfix  : Hotfix branches are used for addressing critical production issues
**Workflow Steps :**

- New features are developed in feature branches and merged back into the develop branch.
- When preparing for a release, a release branch is created from the develop branch.
- Bug fixes for the release are applied in the release branch, and the code is thoroughly tested.
- Once the release is ready, it is merged into both master and develop, creating a new version of the software.
- Hotfixes are treated similarly to releases but are based on the master branch.
- **Version Tagging :**
- After each release or hotfix merge, the master branch is tagged with a version number to mark the release point.

## GitHub Workflow :
- **Forking and Cloning :** 
    - Developers fork a repository to create a personal copy on their GitHub account.
    - They then clone the forked repository to their local machine using git clone.
- **Pull Requests :** 
    - developers submit pull requests from their feature branches to the original repository's main branch.
    - Pull requests initiate code review and discussion, allowing contributors and maintainers to collaborate.
- **Delete your branch :** After you merge your pull request, delete your branch. This indicates that the work on the branch is complete and prevents you or others from accidentally using old branches
