## 1. The Core Architecture

Every Git project moves files through three distinct phases:
- **Working Directory:** Your local folder where you create and edit files (e.g., `peter.txt`, `mj.txt`). Files here are "untracked" or "modified".
- **Staging Area:** A holding zone where you organize exactly what you want to include in your next save.
- **Commit Area (Local Repository):** The permanent historical record of your project.

## 2. Setup & Initialization

- **`mkdir demo-tws`**: Creates the directory.
- **`cd demo-tws`**: Navigates into the directory.
- **`git init`**: Turns a standard folder into a Git repository by creating a hidden `.git/` folder.

## 3. Tracking & Staging Files

- **`git status`**: Checks the current state of your repository. It shows untracked files, modified files, and what is currently in the staging area.
- **`git add .`**: Moves _all_ untracked or modified files from the Working Directory into the Staging Area.
- **`git rm --cached <filename>`**: Unstages a file (e.g., `git rm --cached mj.txt`). This moves the file back to the "untracked" state without deleting the actual file from your computer. 

## 4. Saving Changes (Committing)

- **`git commit -m "your message"`**: Takes a snapshot of everything currently in the Staging Area and saves it to the Commit Area (e.g., `git commit -m "added peter.txt"`).
- _Note:_ If you unstage a file before committing, only the files left in the staging area get saved. You can always `git add` and `git commit` the remaining files later.

## 5. Deleting & Restoring Files from local

- **`rm <filename>`**: A standard terminal command that deletes the file from your local computer's Working Directory.
- **`git restore <filename>`**: Recovers a file you deleted or modified locally, reverting it back to how it looked in your last commit.
- **Committing a deletion:** If you want to permanently remove a file from the Git repository, delete it (`rm`), stage the deletion (`git add .`), and save the change (`git commit -m "removed file"`).
