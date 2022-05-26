# Git cheat sheet

## Pre-Standard
git config --global init.default Branch main

git config --global user.email "sampolgar@gmail.com"

git init | setup dir

ls -la | see in the file structure

rm -rf .git/ | delete the git init file


## Standard

git add . | git add -A

git commit  -m "message"

git status

git remote add origin git remote add origin https://github.com/sampolgar/git-commands.git 

git push --set-upstream origin main

git remote -v

git push -u

## Branch
git branch

git branch sam-feature

git checkout main

git checkout -b sam-newbranch


## Working with upstream repo
git fetch upstream

git merge upstream/main

git push origin main

git pull

## merge fork to main
git checkout main

git pull origin main

git merge test

git push origin main

git log

## add to gitignore
cat gitignore

touch .gitignore

echo 'xxx' > .gitignore

## fork & create pull request
1. clone
2. make fork of originalproject.git
3. make branch on new fork sam-new-branch
3. add files and commit
4. check status
5. git push --set-upstream origin sam-new-branch
6. git remote add upstream https://github.com/originproject.git
7. git fetch upstream
8. git checkout main
9. git merge upstream/main
10. navigate to fork and select pull request

## Links
[Digital Ocean Reference](https://www.digitalocean.com/community/cheatsheets/how-to-use-git-a-reference-guide)

[Atlassian git ignore](https://www.atlassian.com/git/tutorials/saving-changes/gitignore#git-ignore-patterns)