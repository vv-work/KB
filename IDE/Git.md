# Git

## Questions


-  Git stash
-  Git switch
-  Other services except github.
-  Just storage of file archiving?
-  Git LFS ?

## Git gc and archive
Remove unecessary files

`git gc`
`git archive -o latest.zip HEAD`

## Cherry-pck
 
Apply changes introduces by other commit.

## HEAD 

- `HEAD` - Last commit
- `HEAD^^` - two commits ago
- `main~2` - on branch main 2 commit ago

## Restore 
`git restore Readme.md`
`git restore ONe.md --source  d798773f78cf0f3a5430348ae5077723b474e8ec`
`git restore --source main~2 Readme.md`

Restores file from current index or from specific commit
Or Roll back it's content to the state needed

## Stash
It sort of like reset but changes **stashed**
Files basically saying unding changes that was git add

 
## Diff 

```PowerShell
git diff HEAD^
git diff HEAD^^ HEAD^
git diff HEAD COMMIT_ADDRESS
```

## Submodule
The power to add submodule so it will pop up in project
But will be tracked separetly

## Git log

```powershell
git log --follow Readme.md
```

## Add to GIT LFS

```powershell
#file name
git lfs track 'ADDRESS\TO\FILE.type'

```

## Pus local branch to server

```powershell
git branch -u origin <branch name>
```

## Remvoe locak branch

```powershell
git branch -d <branch name>
```

# Remove file from history
    git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch Assets\External\1PumpkinExport\CorryMarryXmas.anim' --prune-empty --tag-name-filter cat -- --all


## SSH

```powershell
ls -al ~/.ssh
# Check is there any files already
```
### Generate

```powershell
ls -al ~/.ssh
$ ssh-keygen -t ed25519 -C "yuriy.paramonov@outlook.com"
# Check is there any files already
```

