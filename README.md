# Git tutorial
Git is a free and open-source version control system.
1. Git helps developers track code changes, work together easily, and go back to previous versions if needed. 
2. It allows multiple people to work on different features at the same time. 
3. Git also keeps code safe and helps with automation, making software development faster, easier, and more organized.
### In simple word
- Tracks Changes – Git saves different versions of your code, so you can go back if needed.
- Works Offline – You don’t need the internet to use Git on your computer.
- Team Collaboration – Many people can work on the same project without messing up each other’s code.
- Branching – You can create separate branches to test new features without affecting the main code.
- Safe & Fast – Git keeps your code safe and makes software development quick and organized.

## 🔗 Links

- **Git download:** [Download](https://git-scm.com/downloads)
- **Git documentation:** [Read Docs](https://git-scm.com/doc)


## 📦 Various git commands used in software industry.
In a simple word, if you are not initiaizing git in you system using **git init** command
you can clone the repo using command.The **.git** folder will created in the folder where you are cloning the repo.

```sh
   git clone <https://rep-you-want-to-clone>
   ```
**Initilize the git**
-This command will initlize the git repo inside your system folder
   ```sh
   git init
   ```
**Check status**
-This command will check the status in which branch you are now. How many file changed and added.

   ```sh
   git status
   ```
**Command to create new branch from base branch**
   ```sh
   git switch -c <new_branch_name>
   git checkout -b <new_branch_name>
   ```
**Commands to add or load the changes into repository**
 - **git add .** OR **git add -A** OR git add * : To add all the file that is appearing in changes
 - **git add <particular_file_name>** : To add particular file from changes appear in changes.
#
   ```sh
   git add . 
   git add file_name_1, file_name_2
   git add *
   git add -A
   ```
**Command to unstages**
   ```sh
   git reset
   git restore <file_name>
   ```
**Command to commit the changes to the repository**
#### amend is use for overwrite the earlier commit message or with --no-edit to update in earlier commit.
   ```sh
   git commit -m "Your_Message_That will_Show_In_Commit_Section"
   git commit --amend --no-edit
   git commit --amend -m "New commit message" 
   ```
   -After the amend command you have to do **--force** if you have pushed the commit earlier.
#
**Command to push the changes to the repository**
   ```sh
   git push -u origin <branch_name>
   git push --set-upstrem origin <branch_name>
   ```
**Command to delete the branch**
   ```sh
   git branch -D <branch_name>
   git branch -d <branch_name> // Delete the branch from remote as well
   ```
**Command to update working branch with base branch**
   ```sh
   git switch <name_of_base_branch>
   git pull 
   git switch <working_branch>
   git merge <name_of_base_branch>
   ```
**Commands to revert the commit**
   ```sh
   git reset --soft HEAD~n //To keep the changes
   git reset --hard HEAD~n //To delete the changes do not want to keep it.
   ```
***Command to see all the commit**
   ```sh
   git log --oneline
   git log
   git log --oneline --graph --decorate --all // To see in graphical view
   ```
**Command to see all history in graphical view**
   ```sh
   gitk --all
   tig --all
   -------------------------------
   UBANTU : sudo apt install tig |
   MAC : brew install tig        |
   ------------------------------   
   ```
**Command to apply one or two commits in one branch from another branch**
   ```sh
   git log --oneline
   a1b2c3d //commit 1
   d4e5f6g //commit 2
   git cherry-pick a1b2c3d
   ```
**If you are trying to push the changes to the repository and you are getting error like below, try this command**
#### error: failed to push some ref's to <https://<name>.com>
   ```sh
   git pull --rebase
   [After that do]
   git push
   [If getting merge conflict resolve it and then]
   git rebase --continue
   git push
   ```
**IIf you are working with group of developers and they have given multiple file with changes or ask you to give your multiple changes in file how you will do that**
#### Try git patch

#### how to create patch file
```sh
git diff > <file_name.patch>
```

#### How to apply patch file
   ```sh
  git apply <file_name.patch>
   ```

#### Note : Download the patch file given by developer & attach to your root of project & in terminal run the apply command


