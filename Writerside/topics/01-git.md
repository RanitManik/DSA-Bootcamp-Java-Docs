# Git & GitHub

## Basic CLI Commands

1. **List all files or folders in a directory:**
   ```bash
   ls
   ```

2. **Make a new folder:**
   ```bash
   mkdir folder_name
   ```

3. **Go inside a folder:**
   ```bash
   cd folder_name
   ```

4. **Delete a whole non-empty directory/folder:**
   ```bash
   rm directory_name -rf
   ```

5. **Write a file in Git Bash Vim:**
   ```bash
   vim file_name
   ```
    - After finishing edits, press the left-right arrow keys to disable writing mode.
    - Write `:x` to exit.

6. **Copy + Paste in CLI:**
    - Use standard copy and paste shortcuts (Ctrl+C, Ctrl+V).

## Basic Git Commands

1. **Make a new file:**
   ```bash
   touch names.txt
   ```

2. **Check if Git is installed:**
   ```bash
   git
   ```

3. **Initialize an empty Git repository:**
   ```bash
   git init
   ```

4. **View changes or untracked files:**
   ```bash
   git status
   ```

5. **Staging files:**
   ```bash
   git add file_name
   ```
   or
   ```bash
   git add .
   ```

6. **Committing files:**
   ```bash
   git commit -m "Your commit message"
   ```

7. **Unstage or remove a file from staging:**
   ```bash
   git restore --staged file_name.txt
   ```

8. **View entire history of the project:**
   ```bash
   git log
   ```

9. **Removing a commit from the history:**
   ```bash
   git reset insert_commit_hash_id_here
   ```

10. **Stash changes for later use:**
    ```bash
    git stash
    ```

11. **Pop changes from the stash:**
    ```bash
    git stash pop
    ```

12. **Clear the stash:**
    ```bash
    git stash clear
    ```

## Working with Existing Projects on GitHub

### Cloning, Branching, and Pushing

1. **Clone a forked project to local machine:**
   ```bash
   git clone forked_repo_url
   ```

2. **Add upstream URL (main project):**
   ```bash
   git remote add upstream insert_upstream_url
   ```

3. **Create a new branch:**
   ```bash
   git branch branch_name
   ```
   then
   ```bash
   git checkout branch_name
   ```

4. **Stage, commit, and push to forked repo:**
   ```bash
   git add .
   git commit -m "Your message"
   git push origin your_branch_name
   ```

5. **Make forked project up-to-date:**
    - Use various methods like fetch, reset, and push to synchronize with the main project.

## Advanced Git Operations

* **Squash multiple commits into one:**
   ```bash
   git rebase -i insert_hash_code_of_commit_above_which_you_want_merged
   ```
  Keep one commit as "pick" and squash the rest.

* **Resolve merge conflicts:**

  Conflicts occur when multiple users edit the same code line. Manual resolution may be required by the repository
  maintainer.

## Additional Resources

For more detailed Git commands and advanced operations, refer to
the [Atlassian Git Cheatsheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet).

Remember, Git and GitHub are powerful tools for version control and collaboration, enabling efficient development
workflows.