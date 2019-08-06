1. in the folder, write in the terminal:
==> git init

2. untracked files are shown
==> git status

3. stage files to add
==> git add test.py
==> git add .

4. show status again
==> git status

5. Create a new version. Each version has its own title.
-m - message
==> git commit -m 'First version of the project!'
==> git commit -am "When something should be deleted use this!"

6. Shows the latest commit
==> git log
to exit log
==> q 
 
6.1. Not needed, a way to register:
git config --global user.name "Vitosh"
git config --global user.email "mail@mail.mail"

7. Shows the different versions
==> git diff

8. Create new repository at github:
==> https://github.com/new

9. Remotes per repository
==> git remote -v
vman@vman-Studio-1555:~/Desktop/TestRepo$ git remote -v
origin	https://github.com/Vitosh/TestRepo.git (fetch)
origin	https://github.com/Vitosh/TestRepo.git (push)

10. Add a remote repository
==> git remote add {Name} {Address}
==>git remote add origin https://github.com/Vitosh/TestRepo.git
"origin" is the name of the repository

11. Push 
==>git push -u origin master

12. Delete remote directory:
==>git remote rm origin

13. 
==>git remote add origin git@github.com:Vitosh/TestRepo.git

14. Make SSH - Secure Shell
-->> https://github.com/settings/profile
https://help.github.com/articles/generating-ssh-keys/ls

15. Pulling
==> git pull origin master

16. History Commits
https://github.com/Vitosh/TestRepo/commits

17. Cloning the repo
==> git clone git@github~

18. Remove directory from git and local
==> git rm -r one-of-the-directories
==> git commit -m "Remove duplicated directory"
==> git push origin master

20. Using branches

==> git branch rado
==> git checkout rado
switched to branch rado

==> git checkout master
==> git push origin rado

==> git branch
=> returns a list of all branches

==> git merge rado
history from rado goes to the master

==> git branch --delete rado
(deletes) local master on the HD
==>git push origin --delete rado
(deletes) master on the cloud

generate collaborator
==> touch B
==> echo "AA" >> B
==> cat B
==> AA

21. Fetch
git pull = git fetch + git merge

22. git remote add upstream https://~

23. git pull --rebase upstream master

24. if you **** ** and you need to reset git:
 git reset --hard a0d3fe6
 where a0d3fe6 is found by doing
 git reflog

25. Git overwrite local files with pull request

git fetch --all
git reset --hard origin/master
git pull origin master


### TLDR:
git add .
git commit -m "some message here"
git status
git push origin master


### Rename repository:
Rename the repository manually. Then run the command to see the new name.
$ git config --list
remote.origin.url=ssh://git@git.example.com/newNameHere.git
Run Git to change the name
$ git remote set-url origin https://git.example.com/newNameHere.git

### Remove Git from local folder
Navigate to the folder
Windows:
del /F /S /Q /A .git
rmdir .git
Linux:
rm -rf .git*

### Overwrite the current changes
Get exact Git from the origin to overwrite the current changes:
git fetch --all
git reset --hard origin/master
https://stackoverflow.com/questions/1125968/how-do-i-force-git-pull-to-overwrite-local-files

### Remove local untracked files:
git clean -n
git clean -f


