<!-- git quick reference -->
## Accidentally Staged a File I didn't Want To
```dotnetcli
git reset -- <path>
```
## A File in The Last Commit is Bad
## I Need to Undo My Changes to a File
### If You Have Not Pushed: Revert a File to Previous Commit:
```dotnetcli
git checkout HEAD~2 -- path/to/file
git commit -m 'reverted to previous commit.'
```
## I Forgot to Add Something to a File I Already Committed
### If You Have Not Pushed: Amend a Commit
After making your change:
```dotnetcli
git add .
git commit --amend --no-edit
```
## The Message in The Last Commit Is Wrong
### If You Have Not Pushed: Amend a Commit
```dotnetcli
git commit --amend -m "<your new message>"
```
### If You Have Pushed and Rewriting History Is Allowed: Amend a Commit
```dotnetcli
git commit --amend -m "<your new message>"
git push --force <branch-name>
```
### Else: You'll Have to Be More Careful Next Time
## I Committed Something to The Main Branch Intended For a New Branch
### If You Have Not Pushed: Copy Main Branch and Remove The Last Commit
```dotnetcli
git branch <my-new-branch>
git reset HEAD~ --hard
git checkout <my-new-branch>
```
### Else: You'll Have to Be More Careful Next Time

## Make a repo bare
```dotnetcli
md ..\repo-bare
git clone --bare ..\repo-bare
cd ..\repo-bare
git update-server-info
```

## Make a repo bare, 2
```dotnetcli
md repo-bare
git clone --bare repo repo-bare
rm -r -fo repo
ren repo-bare repo
cd repo
git update-server-info
```

## Make a bare repo normal
```dotnetcli
git config --local --bool core.bare false
git reset --hard
```
