# Git Bash Cheat Sheet

A useful reference list of Git Bash commands. If there's something missing, please add it!

**Command** | **Description**
----------- | -------------
git config --global user.email <_email address_> | set email
git config --global user.name <_name_> | set username
ssh-keygen -t rsa -b 4096 -C "_email address_" | create ssh key
cd | change directory
ls | list contents of current directory
git clone <_repo key from GitHub_> | clone directory
git status | tells you what branch you are on, what commits have been made and any changes made to files
git add . | stages every file where a change has been made (not really recommended as general good practice)
git add . –n | shows what would be committed but doesn’t carry out any action
git add <_file_> | stages changes made to a particular file
git rm –cached <_file_> | to unstage a file
git commit –m “_Commit message_” | commit staged changes
git push | push commits to GitHub
git pull | pulls from GitHub
git branch | tells you what branch you are on
git branch <_feature/post_name_> | create new branch locally
git checkout <_branch_>	 | change to branch
git checkout –b <_feature/post_name_> | create new branch locally and change to it
git push origin <_feature/post_name_> -u | create branch on GitHub
git log --oneline --graph --decorate --all | creates a neat little summary of the branch history of the repo
git branch –d <_feature/post_name_> | delete branch locally
git diff <_feature/post_name_> | view diff of unstaged file
git revert -n <_commit reference_> | stage new commit to reverse changes made in referenced commit
git reset --mixed <_commit reference_> | delete commits since the referenced commit but retain changes (unstaged)
git reset --hard <_commit reference_> | delete commits since the referenced commit and remove all changes from files
git reset --soft <_commit reference_> | delete commits since the referenced commit but retain changes (staged) 
git commit --amend -m "_commit message_" | amend last commit message
