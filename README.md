# Learning Git

A memory map for the Git command which I use from time to time. These are most used git commands.

1. `git init`<br>
    Use Case: Initializes a new Git repository. This command sets up the necessary Git metadata and prepares the directory for version tracking.<br>
    Example: `git init`<br><br>

2. `git clone [url]`<br>
   Use Case: Makes a clone, or copy, of an existing repository into a new directory. This is typically used to get a local copy of a remote repository.<br>
   Example: `git clone https://github.com/user/repository.git`<br><br>

3. `git add [file]`<br>
   Use Case: Adds files to the staging area in preparation for a commit. This command is used to select specific changes that should be included in the next commit.<br>
    Example: `git add index.html` or `git add .` to add all changes.<br>
    `git commit --amend`: Modifies the most recent commit. This can be used to correct the commit message or to add new changes to the previous commit.<br>
    `git commit --amend -m "Updated commit message"`<br><br>

4. `git commit -m "message"`<br>
    Use Case: Records changes to the repository. Each commit has an associated commit message that explains the changes made.<br>
    Example: `git commit -m "Add initial project files"`<br><br>

5. `git status`<br>
   Use Case: Displays the state of the working directory and the staging area. It lets you see which changes have been staged, which haven't, and which files aren't being tracked by Git.<br>
    Example: `git status`<br><br>

6. `git log`<br>
   Use Case: Shows the commit history for the current branch. This command is used to review the sequence of commits that have been made.<br>
    Example: `git log`<br>
    `git log --graph --decorate --all`: Visualizes the commit history using ASCII art graphs, including branch pointers and tags, which is helpful for understanding the branching and merging history.<br><br>

7. `git pull [remote] [branch]`<br>
    Use Case: Fetches and merges changes from the remote server to your working directory. Commonly used to sync local changes with the remote repository.<br>
    Example: git pull origin main<br><br>

8. `git push [remote] [branch]`<br>
    Use Case: Sends local branch commits to the remote repository branch. This command is used to share your commits with others.<br>
    Example: `git push origin main`<br><br>

9. `git branch`<br>
    Use Case: Lists, creates, or deletes branches. It is used to manage multiple lines of development within the same repository.<br>
    Example: `git branch new-feature` to create a branch.<br><br>

10. `git checkout [branch]`<br>
    Use Case: Switches branches or restores working tree files. This is a key command for navigating between branches.<br>
    Example: `git checkout new-feature`<br><br>

11. `git merge [branch]`<br>
    Use Case: Merges a specified branch into the current branch. This command is used to integrate changes from one branch into another.<br>
    Example: `git merge new-feature`<br><br>

12. `git rebase [branch]`
    Use Case: Applies changes from one branch onto another without creating a merge commit. This is often used to maintain a linear project history.
    Example: `git rebase main`<br>

13. `git stash`<br>
    Use Case: Temporarily stores all modified tracked files and stages changes to be revisited later on. Useful for switching contexts without committing unfinished work.<br>
    Example: `git stash`<br><br>

14. `git tag [tag-name]`<br>
    Use Case: Marks specific points in history as important. Typically used to mark release points (v1.0, v2.0, etc.).<br>
    Example: `git tag v1.0.0`<br><br>

    `git tag -a v1.0 -m "Release version 1.0"`<br>
        Use Case: Creates an annotated tag. Tags are used to mark specific points in history as being important, typically used for releases.<br>
        Example: `git tag -a v1.0 -m "Release version 1.0"`<br>
    `git push --tags`<br>
        Use Case: Pushes all local tags to the remote repository.<br>
        Example: `git push --tags`<br><br>

15. `git diff`<br>
    Use Case: Shows the differences between two Git data points, such as branches, commits, and more. Useful for code reviews and comparing changes.<br>
    Example: `git diff`<br><br>

16. `git config`<br>
    Use Case: Sets or gets Git configuration settings. Crucial for configuring user information, remote repository settings, and more.<br>
    Example: `git config --global user.name "Your Name"`<br><br>

17. `git remote add [name] [url]`<br>
    Use Case: Adds a new remote Git repository as a shortcut you can reference easily.<br>
    Example: `git remote add origin https://github.com/user/repo.git`<br><br>

18. `git fetch [remote]`<br>
    Use Case: Downloads all changes from the remote repository, but doesn't integrate any of this new data into your working files. It's useful for viewing what others have done without merging those changes into your own branches.<br>
    Example: `git fetch origin`<br><br>

19. `git reset`<br>
    Use Case: Resets your index (staging area) and working directory to the state of a specified commit. Various options (--soft, --mixed, --hard) dictate how thorough the reset is.<br>
    Example: `git reset --hard HEAD~1` (Dangerously resets the current branch to the state of the commit one step back, discarding all intervening changes)<br><br>

20. `git revert [commit]`<br>
    Use Case: Creates a new commit that undoes the changes from a specified commit. This is a safe way to undo changes and share the undo with others.<br>
    Example: `git revert 1a2b3c4`<br><br>

21. `git lfs`<br>
    `git lfs track "*.psd"`<br>
        Use Case: Tracks large files with Git Large File Storage (LFS), preventing them from bloating the repository size.<br>
        Example: `git lfs track "*.psd"`<br>
    `git lfs ls-files`<br>
        Use Case: Lists the files being tracked by Git LFS.<br>
        Example: `git lfs ls-files`<br><br>

22. `git submodule`<br>
    `git submodule add [url] [path]`<br>
        Use Case: Adds a new submodule to your project. Submodules allow you to keep a Git repository as a subdirectory of another Git repository.<br>
        Example: `git submodule add https://github.com/username/repo lib/repo`<br>
    `git submodule update --init --recursive`<br>
        Use Case: Updates the submodules, initializing and updating them and any nested submodules.<br>
        Example: `git submodule update --init --recursive`<br><br>

23. `git show [commit]`<br>
    Use Case: Shows various types of objects (commits, tags, etc.), typically used to view information about specific commits.<br>
    Example: `git show 1a2b3c4d`<br><br>

24. `git blame [file]`<br>
    Use Case: Shows what revision and author last modified each line of a file. It's particularly useful for figuring out who made specific changes.<br>
    Example: `git blame index.html`<br><br>

25. `git clean`<br>
    `git clean -n`<br>
        Use Case: Shows which untracked files would be removed from the working directory (without actually removing them).<br>
        Example: `git clean -n`<br>
    `git clean -f`<br>
        Use Case: Removes untracked files from the working directory.<br>
        Example: `git clean -f`<br><br>

26. `git format-patch HEAD~3`<br>
    Use Case: Creates patch files for the last 3 commits, which can be emailed or used elsewhere.<br>
    Example: `git format-patch HEAD~3`<br><br>

27. `git apply [patch-file]`<br>
    Use Case: Applies a patch file to your working directory.<br>
    Example: `git apply fix.patch`<br><br>

28. `git rm [file]`<br>
    Use Case: Removes files from the working directory and the index (staging area), effectively staging them for deletion.<br>
    Example: `git rm file.txt`<br>
    Note: After using git rm, you need to commit the change.<br><br>

29. `git mv [old-file] [new-file]`<br>
    Use Case: Moves or renames a file, directory, or symlink, automatically staging the change for the next commit.<br>
    Example: `git mv old_name.txt new_name.txt`<br><br>

30. `git restore [file]`<br>
    Use Case: Restores files in the working directory. Useful for discarding changes in the working directory.<br>
    Example: `git restore file.txt`<br><br>

31. `git restore --staged [file]`<br>
    Use Case: Unstages a file while retaining the changes in the working directory.<br>
    Example: `git restore --staged file.txt`<br><br>

32. `git cherry-pick [commit]`<br>
    Use Case: Applies the changes introduced by some existing commits to the current branch. Useful for pulling individual changes from another branch without merging full branches.<br>
    Example: `git cherry-pick 4a5e6f7`<br><br>

33. `git describe [commit]`<br>
    Use Case: Gives a human-readable description of a commit, typically describing how far a commit is from an annotated tag.<br>
    Example: `git describe --tags`<br><br>

34. `git worktree add [path] [branch]`<br>
    Use Case: Manages multiple working trees attached to the same repository, allowing you to check out multiple branches at once.<br>
    Example: `git worktree add ../new-worktree experiment-branch`<br><br>

35. `git grep [pattern]`<br>
    Use Case: Lets you search through your tracked files in the working directory for a string or regular expression.<br>
    Example: `git grep "initializeApp"`<br><br>

36. `git bisect start`<br>
    Use Case: Uses binary search to find the commit that introduced a bug. You start by marking a known bad commit and a known good commit, and Git helps you narrow down to the exact commit introducing the bug.<br>
    Example: `git bisect start; git bisect bad; git bisect good 1a2b3c4`<br><br>

37. `git shortlog`<br>
    Use Case: Summarizes git log output. It groups commit entries by author and can be used to quickly understand the contribution breakdown.<br>
    Example: `git shortlog`<br><br>

38. `git archive`<br>
    Use Case: Creates an archive (such as a tar or zip file) of files from a named tree (commit, branch, or tag).<br>
    Example: `git archive --format=zip HEAD > project.zip`<br><br>


## Case Study

### 1. Go back to working commit
Let's say you have pushed a piece of code but realizes that it was a huge mistake. And now you want to go back to your previous commit and discard all the changes that you did. <br>
This generates two scenario, do we want to keep a record of changes that we made or do we not want to keep a record of the changes. <br><br>
Let's say we want to safely undo changes without rewriting history:<br><br>
a. Let's identify the commit id which you want to revert to.
```
git log
```
b. Then let's revert safely to the commit.
```
git revert <commit-id>
```
c. Finally push the changes:
```
git push origin <branch-name>
```
<br>
Now let's say we don't want to keep any record and go back to the specific commit id.<br><br>
a. Let's identify the commit id which you want to revert to.

```
git log
```
b. Reset to the commit.
```
git reset --hard <commit-id>
```
c. Finally push tha changes
```
git push --force origin <branch-name>
```
<br><br>



### 2. Rebasing the branch

You are working on a feature branch `feature-xyz` while other developers are also making changes on the `main` branch. Your goal is to integrate your changes from `feature-xyz` into the `main` branch in a clean, linear history. Instead of merging main into your feature branch and then merging the feature branch back into `main`, you decide to use rebase to make the history more readable.<br><br>
Let's checkout the `feature-xyz` branch and make some changes to it and commit those changes.<br>
```
git checkout feature-xyz
```
Made some changes in the and did the commit. But realized that there had been changes in the `main` branch by other developers. So let's go ahead and rebase it.

```
git fetch origin
git checkout main
git pull origin main
git checkout feature-xyz
git rebase main
```
Now at this point if you have some conflicting commits. The resolve it manually and then continue with the following command.
```
git add <resolved-file>
git rebase --continue
```
Finally push the changes once when all the conflicts has been pushed.
```
git push --force origin feature-xyz
```

Note: One can also use `merge` in this scenario but you would like to use `rebase` when you want to want to keep the history of the commits in linear manner.<br><br>

### 3. Cherry Picking the changes
You are working on a feature branch (`feature-A`) and realize that one specific commit from another branch (`feature-B`) contains a critical bug fix that you need in your current branch. Instead of merging the entire `feature-B` branch, you decide to cherry-pick just the necessary commit to apply the fix to your `feature-A` branch.<br><br>
a. Let's say you made some changes and committed on the `feature-A` branch (also you can push here) and realized that there had been some bug fixes in the `feature-B` branch which you want to cherry-pick.
```
git fetch origin feature-B
git checkout feature-B
git pull
git checkout feature-A
git log feature-B
```
Here you can note the commit-id from `feature-B` which has the bug fix and then go ahead and apply them.
```
git cherry-pick <commit-id>
```
If there are any conflicts, then resolve it.
```
git add <resolved-file>
git cherry-pick --continue
```
Once all the fixes has been done then go ahead commit them and push them.
```
git push origin feature-A
```
<br>

### 4. Effective Git Branching and Merging
You are part of a development team working on a project with a standard Git workflow. Your team uses feature branches to develop new features and fixes, which are eventually merged into the main branch. You will demonstrate how to create and manage branches, as well as merge them back into the main branch effectively. <br><br>

a. Let's say you want to go to `feature-A` branch and make some changes and commit those changes.
```
git checkout origin feature-A
echo 'hello' > index.html
git add index.html
git commit -m "WIP: working on index"
git push origin feature-A
```
b. At this point you realized there are some updates on the `main` branch and you want to keep your current `feature-A` branch up to date.
```
git pull origin main
```
If there are any conflicts, then resolve it manually and then add them and commit them.
```
git add <resolved-file>
git commit -m "FIX: resolved commits"
```
c. Continue working on your `feature-A` branch until your work is done and then finally commit all the changes. Once your work with the feature is done, we will merge this with the `main` branch.
```
git checkout main
git merge feature-A
git push origin main
```