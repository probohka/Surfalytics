## status
To check if the current local version is equal with current on the git


## pull
Download the newest code from your remote server (like GitHub):
~~~
git pull
~~~
The git pull command is actually a two-in-one shortcut. It automatically runs a fetch followed by a merge:
git pull = git fetch (download data) + git merge (force it into your local working files)


## fetch
You use fetch command and see what your teammates worked on before deciding to mix it into your local project.

The git fetch command downloads the latest history, branches, and tags from your remote repository (like GitHub) to your local machine, without changing any of your local files.

```
git fetch
```


## merge
Run merge for find differences in files
```
git merge
```

## checkout (this is the old version! look at switch and restore)
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


## switch 
Just switch branch
```bash
git switch branchName
```

**Create and switch**: Create a new branch and immediately move into it.

```
git switch -c <branch-name>
```

**IMPORTANT**
Always — you see, always! — before starting work, a programmer should create their own new branch! It doesn't matter what repo they use, whether it’s a shared repository workflow or a forking workflow. Before you need create a Branch!

### restore 

To discard all uncommitted changes in your current directory and its subdirectories, use the dot (.) shortcut:
```bash
git restore .
```

If you have already staged files and want to wipe everything out completely, you have to run:
```bash
git restore --staged .
```


## Send changes to the server
Save changes if not! Because GIT can add and push changes that only saved on the disk (ctrl+s on EDI or autosave). 

### 1. add - Stage changes
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
### 2. commit
Fill in comments

### 3. pull
Get latest version of main branch.
See at pull command

```bash
git pull origin main
```

### 4. push
send changes to the server

```bash
git push
```


## Workflow summary
1. Clone Prod code git clone
2. Create dev branch git checkout -b branch-name
3. do the code changes
4. check what we have modified git status .
5. Index modified files git add .
6. Commit these files git commit -m "Message"
7. Push to remote: git push
8. Create Pull Request for Code review
