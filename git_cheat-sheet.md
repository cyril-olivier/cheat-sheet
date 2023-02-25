# git cheat-sheet

## Genrate RSA keys
```
ssh-keygen -t rsa -b 4096 -f git_rsa

ls -1
---
git_rsa
git_rsa.pub
---

cat git_rsa.pub
---
ssh-rsa ...
---
```


## Add public key to github

*Settings/SSH and GPG Keys/New SSH key*
```
Title: My github_key
Key type: Authentication key
Key: PASTE git_rsa.pub
==> Add SSH key
```

## Make .gitignore

*Add .gitignore file in root folder project*
```
vim .gitignore
---
.gitignore
venv
---
```


## Make new project in github

*Repositories/New*
```
Repository name: cheat-sheet
Description (optional): My cheat-sheet
o Public
o Private
==> Create repository
```


## Create new repository
```
echo "# cheat-sheet" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:cyril-olivier/cheat-sheet.git
git push -u origin main
```


## Check status of project (files modified)
```
git status
```


## Commit change
```
git add git_cheat-sheet.md
git commit -am 'Add ./git_cheat-sheet.md'
git push
```


## Display banch
```
git branch
```


