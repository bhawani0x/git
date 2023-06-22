# Git Commands for Remote Repositories

1. **git remote add <name> <url>**

   Create a new connection to a remote repository. After adding a remote, you can use `<name>` as a shortcut for `<url>` in other commands.

   Example:
   ```
   git remote add origin https://github.com/exampleuser/example-repo.git
   ```

2. **git pull <remote>**

   Fetch the specified remote's copy of the current branch and immediately merge it into the local copy.

   Example:
   ```
   git pull origin
   ```

3. **git push <remote> <branch>**

   Push the branch to `<remote>`, along with necessary commits and objects. Creates a named branch in the remote repo if it doesn't exist.

   Example:
   ```
   git push origin main
   ```

4. **git status**

   List which files are staged, unstaged, and untracked.

   Example:
   ```
   git status
   ```

5. **git commit -m "<message>"**

   Commit the staged snapshot, but instead of launching a text editor, use `<message>` as the commit message.

   Example:
   ```
   git commit -m "Added new feature"
   ```

6. **git add .**

   Stage all changes in `<directory>` for the next commit. Replace `<directory>` with a `<file>` to change a specific file.

   Example:
   ```
   git add .
   ```

7. **git rebase <base>**

   Rebase the current branch onto `<base>`. `<base>` can be a commit ID, branch name, a tag, or a relative reference to HEAD.

   Example:
   ```
   git rebase main
   ```

8. **git rebase -i <base>**

   Interactively rebase current branch onto `<base>`. Launches an editor to enter commands for how each commit will be transferred to the new base.

   Example:
   ```
   git rebase -i main
   ```

9. **git clone <url>**: This command is used to clone a remote repository and create a local copy on your machine. It copies the entire repository, including all branches and commit history. For example:
   ```
   git clone https://github.com/exampleuser/example-repo.git
   ```
   This clones the remote repository located at `https://github.com/exampleuser/example-repo.git` to your local machine.

10. **git remote -v**: This command lists all the remote repositories connected to your local repository along with their URLs. It shows the fetch and push URLs of each remote repository. For example:
    ```
    git remote -v
    ```
    This command displays a list of remote repositories and their URLs.

11. **git fetch <remote>**: This command fetches the latest changes from the specified remote repository without merging them into your local branch. It updates the remote-tracking branches. For example:
    ```
    git fetch origin
    ```
    This fetches the changes from the `origin` remote repository.

12. **git branch -r**: This command lists all the remote branches in the remote repository. It shows the branches available in the remote repository without checking them out locally. For example:
    ```
    git branch -r
    ```
    This lists all the remote branches.

13. **git branch -a**: This command lists all the local and remote branches in your repository. It displays both local branches and remote branches. For example:
    ```
    git branch -a
    ```
    This lists all the local and remote branches.

14. **git branch <branch_name>**: This command creates a new branch with the given name. It creates a new branch at the current commit. For example:
    ```
    git branch feature-branch
    ```
    This creates a new branch named `feature-branch`.

15. **git checkout <branch_name>**: This command is used to switch to the specified branch. It updates the working directory to match the selected branch. For example:
    ```
    git checkout feature-branch
    ```
    This switches to the `feature-branch` branch.

16. **git merge <branch_name>**: This command merges the specified branch into the current branch. It combines the changes from the specified branch into the current branch. For example:
    ```
    git merge feature-branch
    ```
    This merges the changes from the `feature-branch` into the current branch.

17. **git branch -d <branch_name>**: This command deletes the specified branch. It removes the branch reference and its commit history. For example:
    ```
    git branch -d feature-branch
    ```
    This deletes the `feature-branch`.

18. **git push <remote> --delete <branch_name>**: This command deletes the specified branch from the remote repository. It removes the branch from the remote repository's references. For example:
    ```
    git push origin --delete feature-branch
    ```
    This deletes the `feature-branch` from the `origin` remote repository.

19. **git remote rename <old_name> <new_name>**: This command is used to rename a remote repository. It renames the reference to a remote repository in your local repository. For example:
    ```
    git remote rename origin upstream
    ```
    This renames the remote repository from `origin` to `upstream`.

20. **git reset <commit>**: This command resets the current branch to a specific commit, discarding all subsequent commits. It moves the branch pointer and resets the staging area. For example:
    ```
    git reset HEAD~1
    ```
    This resets the branch to the previous

 commit, discarding the latest commit.

21. **git diff**: This command shows the changes between the working directory and the staging area. It displays the differences in the content of files that are not yet staged. For example:
    ```
    git diff
    ```
    This shows the differences between the working directory and the staging area.

22. **git stash save**: This command saves the current changes in a stash, allowing you to switch to a different branch without committing them. It stores the changes temporarily. For example:
    ```
    git stash save "Work in progress"
    ```
    This saves the current changes with a message "Work in progress."

23. **git stash pop**: This command applies the most recently saved stash and removes it from the stash list. It restores the changes previously stashed. For example:
    ```
    git stash pop
    ```
    This applies the most recent stash and removes it from the stash list.

24. **git stash list**: This command lists all the stashes saved in your repository. It displays the stash index and message for each saved stash. For example:
    ```
    git stash list
    ```
    This lists all the stashes saved in the repository.

25. **git stash drop <stash_name>**: This command deletes a specific stash from the stash list. It removes the specified stash and its changes. For example:
    ```
    git stash drop stash@{0}
    ```
    This deletes the stash with the name `stash@{0}`.
