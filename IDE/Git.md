# Typical git upload code
git branch -M main
git remote add origin git@github.com:ComanGames/GeeneeMasks.git
git push -u origin main


# Add to GIT LFS
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