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