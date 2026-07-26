### git status
To check if the current local version is equal with current on the git

### checkout (this is the old version! look at switch and restore)
Create new branch with the your name, and used to switch between different branches or restore working tree files.

Create a brand new branch and immediately switch to it using the -b flag.
```bash
git checkout -b branchName
```
Move from your current branch to an existing branch to work on different code.

```bash
git checkout feature-login
```
The git checkout command is primarily used to switch between different branches or restore working tree files


### switch 
Just switch branch
```bash
git switch branchName
```

**Create and switch**: Create a new branch and immediately move into it.
```
git switch -c <branch-name>
```

### restore 

To discard all uncommitted changes in your current directory and its subdirectories, use the dot (.) shortcut:
```bash
git restore .
```

If you have already staged files and want to wipe everything out completely, you have to run:
```bash
git restore --staged .
```

### add - Stage changes
Tells Git to gather and stage all your local changes so they are ready to be included in your next commit. 

Tell Git which modifications you want to package up (the dot flags all changes in your folder).

Add file contents to the index.

Add all files:
```
git add .
```

or certain file
```
git add fileName
```






python3 -m pip install pre-commit

pre-commit --version

pre-commit 3.5.0


 pre-commit install

pre-commit installed at .git/hooks/pre-commit

```
repos:
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v3.4.0  # Use the latest version
    hooks:
    -   id: trailing-whitespace
    -   id: end-of-file-fixer
    -   id: check-yaml
```

Instal YAML
pre-commit install

Test:
pre-commit run --all-files




mkdir -p .github/workflows


touch .github/workflows/pre_commit.yml

```
name: Pre-Commit

on: [push, pull_request]

jobs:
  pre-commit:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - uses: actions/setup-python@v2
      with:
        python-version: '3.x'
    - name: Install pre-commit
      run: pip install pre-commit
    - name: Run pre-commit on all files
      run: pre-commit run --all-files
```


git add .github/workflows/pre_commit.yml
git commit -m "Add GitHub Actions workflow for pre-commit"
git push
