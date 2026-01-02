# Git Commands Used

This document lists the Git commands used while completing Task 1 (Git & GitHub) during my DevOps internship tasks.

---

## Repository Setup

```bash
git clone https://github.com/tobifotis/DevOps-internship-task.git
cd DevOps-internship-task
```

Clones the remote repository and navigates into the project directory.

---

## Creating the First Commit (master branch)

```bash
mkdir Task1
echo # Task 1: Git and GitHub > Task1/README.md
git add Task1/README.md
git commit -m "Initial commit: add Task1 README"
git push -u origin master
```

Creates the initial project structure and pushes the first commit to the `master` branch.

---

## Creating and Using the dev Branch

```bash
git checkout -b dev
echo test > test.txt
git add test.txt
git commit -m "Add test file"
git push -u origin dev
```

Creates the `dev` branch, adds a test file, and pushes it to GitHub.

---

## Creating the Feature Branch

```bash
git checkout -b tobifotis-new_feature
git push -u origin tobifotis-new_feature
```

Creates and tracks a feature branch for isolated development.

---

## Adding Files on the Feature Branch

```bash
echo # Feature branch README > README.md
git add README.md
git commit -m "Add README on feature branch"
git push
```

Adds a README file to the feature branch and pushes the changes.

---

## Checking Repository Status

```bash
git status
```

Displays the current branch and the working tree status.

---

## Adding a .gitignore File

```bash
echo .* > .gitignore
echo !.gitignore >> .gitignore
git add .gitignore
git commit -m "Add .gitignore"
git push
```

Creates a `.gitignore` file to ignore files starting with `.` while ensuring `.gitignore` itself is tracked.

---

## Reverting a Commit

```bash
git revert HEAD
git push
```

Creates a new commit that reverses the changes introduced by the most recent commit.

---

## Viewing Commit History

```bash
git log
```

Displays the commit history of the repository.

---

## Saving Commit History to a File

```bash
git log > log.txt
git add log.txt
git commit -m "Add git log output"
git push
```

Saves the commit history to `log.txt` and pushes it to the repository.

---

## Deleting Branches

```bash
git checkout dev
git branch -D tobifotis-new_feature
git push origin --delete tobifotis-new_feature
```

Deletes the local and remote feature branch after it is no longer needed.
