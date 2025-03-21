# Git Commands

This document provides a list of useful Git commands for version control.

## Git Configuration Commands

### `git config --global user.name "Your Name"`
- Sets the global Git username for commits.

### `git config --global user.email "your.email@example.com"`
- Sets the global Git email address for commits.

### `git config --list`
- Lists all Git configuration settings.

### `git config --global core.editor <editor>`
- Sets the default editor for Git (e.g., `vim`, `nano`, `code`).

## Git Repository Commands

### `git init`
- Initializes a new Git repository in the current directory.

### `git clone <repository_url>`
- Clones a remote repository to the local machine.

### `git status`
- Displays the status of the working directory and staging area.

### `git diff`
- Shows changes between the working directory and the staging area.

### `git add <file>`
- Stages a file for commit.

### `git add .`
- Stages all modified files in the working directory for commit.

### `git commit -m "Commit message"`
- Commits the staged changes with a message.

### `git commit --amend`
- Modifies the last commit (e.g., to change the commit message).

### `git log`
- Displays the commit history for the current branch.

### `git log --oneline`
- Displays a condensed commit history (one line per commit).

### `git log --graph`
- Displays the commit history as a graph.

### `git show <commit_hash>`
- Displays detailed information about a specific commit.

### `git reset <file>`
- Unstages a file (removes it from the staging area).

### `git reset --hard`
- Resets the working directory and staging area to the last commit (dangerous!).

### `git rm <file>`
- Removes a file from the working directory and stages the removal for commit.

## Git Branching Commands

### `git branch`
- Lists all branches in the repository.

### `git branch <branch_name>`
- Creates a new branch with the specified name.

### `git branch -d <branch_name>`
- Deletes a local branch.

### `git checkout <branch_name>`
- Switches to an existing branch.

### `git checkout -b <branch_name>`
- Creates and switches to a new branch.

### `git merge <branch_name>`
- Merges the specified branch into the current branch.

### `git rebase <branch_name>`
- Rebases the current branch onto the specified branch.

### `git stash`
- Stashes changes in the working directory that are not ready to commit.

### `git stash pop`
- Applies the most recent stash and removes it from the stash list.

### `git stash list`
- Lists all stashed changes.

### `git checkout -- <file>`
- Discards changes in the working directory for the specified file.

## Git Remote Commands

### `git remote add <remote_name> <repository_url>`
- Adds a remote repository to the local Git repository.

### `git remote -v`
- Lists all remotes associated with the repository.

### `git fetch <remote_name>`
- Fetches changes from a remote repository without merging them into the current branch.

### `git pull <remote_name> <branch_name>`
- Fetches changes from a remote repository and merges them into the current branch.

### `git push <remote_name> <branch_name>`
- Pushes commits to a remote repository on the specified branch.

### `git push --set-upstream <remote_name> <branch_name>`
- Sets the upstream branch for the current branch and pushes changes.

### `git push --force`
- Forces a push to the remote repository, overwriting history (use with caution).

### `git push origin --delete <branch_name>`
- Deletes a branch from the remote repository.

### `git remote remove <remote_name>`
- Removes a remote repository from the local repository.

## Git Tagging Commands

### `git tag`
- Lists all tags in the repository.

### `git tag <tag_name>`
- Creates a new tag at the current commit.

### `git tag -a <tag_name> -m "Tag message"`
- Creates an annotated tag with a message.

### `git push <remote_name> <tag_name>`
- Pushes a tag to the remote repository.

### `git push --tags`
- Pushes all tags to the remote repository.

### `git tag -d <tag_name>`
- Deletes a tag locally.

### `git push <remote_name> --delete <tag_name>`
- Deletes a tag from the remote repository.

## Git Undoing Changes Commands

### `git revert <commit_hash>`
- Creates a new commit that undoes the changes made by the specified commit.

### `git reset <commit_hash>`
- Resets the current branch to the specified commit, leaving changes in the working directory.

### `git reset --soft <commit_hash>`
- Resets the current branch to the specified commit, keeping changes in the staging area.

### `git reset --hard <commit_hash>`
- Resets the current branch to the specified commit and discards changes in the working directory.

## Git Merge Conflicts Resolution

### `git mergetool`
- Opens a tool to resolve merge conflicts.

### `git merge --abort`
- Aborts a merge in progress and restores the repository to its previous state.

## Git Fetching Changes Commands

### `git fetch`
- Fetches changes from the remote repository but does not merge them into the current branch.

### `git pull`
- Fetches and merges changes from the remote repository into the current branch.

## Git Rewriting History Commands

### `git rebase -i <commit_hash>`
- Initiates an interactive rebase to rewrite commit history (e.g., to squash or reorder commits).

### `git filter-branch --tree-filter <command>`
- Rewrites commit history by applying a filter to all commits.

### `git reflog`
- Shows the history of branch changes and commits, including reset and rebase actions.

## Git Submodule Commands

### `git submodule add <repository_url> <path>`
- Adds a new submodule to the repository.

### `git submodule init`
- Initializes all submodules in the repository.

### `git submodule update`
- Updates the submodules to match the commit specified in the main repository.

### `git submodule update --remote`
- Updates the submodules to the latest commit on their respective branches.

### `git submodule deinit <path>`
- Removes the submodule from the repository.

## Other Useful Git Commands

### `git archive --format=zip --output=<file.zip> <branch_name>`
- Creates an archive of the specified branch or commit.

### `git gc`
- Cleans up unnecessary files and optimizes the local repository.

### `git fsck`
- Checks the integrity of the repository and reports any issues.

### `git bisect start`
- Starts a bisect session to find which commit introduced a bug.

### `git bisect bad`
- Marks the current commit as "bad" during a bisect session.

### `git bisect good <commit_hash>`
- Marks a specific commit as "good" during a bisect session.

### `git bisect reset`
- Ends the bisect session and returns the repository to its original state.

### `git ls-files`
- Lists all files in the repository that are tracked by Git.

### `git rev-parse <commit>`
- Resolves a commit hash, branch name, or other reference to a specific Git object.

### `git submodule status`
- Shows the status of all submodules in the repository.
