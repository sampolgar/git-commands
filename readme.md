# Git cheat sheet

## Setup Project
git config --global init.default Branch main

git config --global user.email "sampolgar@gmail.com"

git init | setup dir

ls -la | see in the file structure

rm -rf .git/ | delete the git init file

## Create New Repo

git add README.md

bit branch -M main

git remote add origin https://github.com/sampolgar/project.git

git add .

git commit -m "initial"

git push -u origin main

## Push exisiting repo
git remote add origin https://github.com/sampolgar/project.git

git branch -M main

git push -u origin main

## Adding/Committing/Status

git add . | git add -A

git commit  -m "message"

git status

git remote add origin https://github.com/sampolgar/git-commands.git 

git push --set-upstream origin main

git remote -v

git push -u

## Branch
git branch

git branch -r

git branch sam-feature

git checkout main

git checkout -b sam-newbranch

git branch -d (delete branch locally, branch must be committed)

git branch -D (delete branch, doesn't need commit, ensure you're on the branch)


# Early Troubleshooting

git remote set-url origin https://github.com/sampolgar/new-remote-url.git


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

## standard linux

mv commands.md readme.md

rm readme.md

rm-r

## fork & create pull request
1. clone
2. make fork of originalproject.git
3. make branch on new fork sam-new-branch
3. add files and commit
4. check status
5. git push --set-upstream origin sam-new-branch
6. git remote add upstream https://github.com/username/originproject.git
7. git fetch upstream
8. git checkout main
9. git merge upstream/main
10. navigate to fork and select pull request

## Merge project A into Project B
cd path/to/project-b

git remote add project-a /path/to/project-a

git fetch project-a --tags

git merge --allow-unrelated-histories project-a/master # or whichever branch you want to merge

git remote remove project-a

## bash
find: sudo find . -name "*poster*"

rename file: mv filename newfilename

# Troubleshooting
### refusing to merge unrelated histories
Because there is no common base - when I created a new project and pushed it as a branch

--allow-unrelated-histories

### when you didn't make any change but git says theres a change. Check status, then if not needed
git reset --hard

### .DS_Store causing trouble
Delete it
find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch

Add it to gitignore
echo .DS_Store >> .gitignore

Commit
git add .gitignore
git commit -m '.DS_Store banished!'

# Ancillary

## Ngrok
- download and unzip ngrok
- ngrok config add-authtoken {authtoken}
- ngrok http 3000

## Deno
- cmd, shift, P - run -> Deno: Initialize Workspace Configuration command

## Links
[Digital Ocean Reference](https://www.digitalocean.com/community/cheatsheets/how-to-use-git-a-reference-guide)

[Atlassian git ignore](https://www.atlassian.com/git/tutorials/saving-changes/gitignore#git-ignore-patterns)
