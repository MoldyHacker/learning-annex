# Git - https://git-scm.com/
![The Git Logo](assets/Git-Logo-2Color.svg "The Git Logo")

>Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

## Download, Install & Setup
This part maybe slow and self explanitory for some.

### Download
1. Proceed to the website https://git-scm.com/downloads and download the latest version of Git that correlates to your computer's OS. (Should be the version diplayed by default on the page)

### Install
2. Install said software with default values. (If there are particular setting you know you want, choose them now)
    1. Run installer
    2. Select Components
    3. Choosing the default editor used by Git
        > Vim is the default editor of Git for windows only for *historical reasons*, and it is highly recommended to switch to a modern GUI editor instead.
        - If the description of the editor is grayed out, it has been deprecated and can no longer be used.
        - Modern editors:
            - Visual Studio Code (VSCode)
            - Notepad++
        - But the choice is ultimatley whatever text editor you are most comfortable with.
    4. Adjusting the name of the initial branch in new repositories.
        - You can *Let Git decided* but
            > the Git project [intends](https://sfconservancy.org/news/2020/jun/23/gitbranchname/) to change this default (master) to a more inclusive name in the near future.
        - As such it is recommended to choose **Override the default branch name for new repositories** with the override being "main"
    5. For the rest of the options default  
    [Git Credential Manager](https://github.com/git-ecosystem/git-credential-manager)  
    [Info about GCM](https://github.com/git-ecosystem/git-credential-manager/blob/HEAD/docs/faq.md#about-the-project)

### Setup
3. After you finish installing Git, you're going to need to setup the config a bit. To do that we will need to open a Git Terminal, either GitBash or GitCMD will work for this. Once open we will begin setup.
    1. #### Name Setup
    Attached your name to Git. This is very important because this name will be attached to every commit you make. You have two options with this. You cam attach your first and last names, or you can enter your chosen username that you associate with a *Git Repo Service* such as **GitHub**.  
    Run the following command in the Git Terminal(remove the square brackets entering your information, but leave the quotes):  
    ``git config --global user.name "[firstname lastname]"``  
    or  
    ``git config --global user.name "[name]"``  
    The ``--global`` flag assigns this name to the entire computer config.


    2. #### Email Setup
    Attach your email to Git. Arguably just as important as the name attached, this is the email you associate with your Git. If you are using an online service such as **GitHub** you should use the email associated with that account. (GitHub has an anonymous email you can use to links your username.)  
    Run the following
    Command in the Git
    Terminal(remove the
    square brackets entering your information, but leave the quotes):  
    ``git config --global user.email "[email@email.com]"``  

    3. #### Basic Config Options
    - The following command setups the colors in the Git CMD and Bash  
    ``git config --global color.ui auto``

    - this command sets your default branch name to *main* from the antiquated *master*, if you didn't do that in the inital setup when installing Git.  
    ``git config --global init.defaultBranch main``

## Baisc Commands
Most modern IDE's have integrated and easy ways to perform most, if not all of these operations. Later we can go over how to perform them in a couple of popular IDEs.

### Initializing a Git Repository

#### Create a New local Repo

``git init``  
or   
``git init [project name]``  
This command will initialize a new local Git repo. If you provide a *project name* after the command(excluding the square brackets) Git will create a new directory with the included *project name*

#### Download a Remote Repo

``git clone <url.git>``
Downloads a project and the entire git history from a remote repo hosted on a service such as **GitHub**  
The **.git** extension is ***important*** 

### Stage & Snapshot

``git status``  
Show the status of the files in your working directory and staged for the next commit.

``git add [file]``  
Add a file to the staging area. Instead of the full file path, use the current directory down into the directory tree.  

``git diff [file]``  
Shows the difference between the working directory and the staging area.

``git diff --staged [file]``  
Shows differences between **staging area** and **repository**  

``git checkout --[file]``  
Discard changes in working directory. **This operation is *unrecoverable***

``git reset [file]``  
Unstage a file while retaining the changes in the working directory.

``git commit -m "[descriptive message]"``  
Commit your staged changes.

### Redo Commits

``git reset [commit]``  
Undoes all commits after the spcified commit preserving all changes locally.  

``git reset --hard [commit]``  
Discards all changes and history back to the spcified commit.

### Path Changes

``git rm [file]``  
Remove the file from the project and stage the removal for commit.

``git mv [existing-path] [new-path]``  
Change an existing file path and stage the move for commit.

``git log --stat -M``  
Display all commit logs relating to any paths that moved.

### Branch & Merge

``git branch``  
List all branches. (An a* will appear next to the currently active branch)

``git branch [branch-name]``  
Create a new branch with the current commit.

``git checkout [branch-name]``  
Switch to the specified branch and updates the working directory.  

``git merge [branch]``  
Merge the specified branch into the current one.  

``git branch -d [branch]``  
Deletes specified branch.    

``git log``
Displays all commits in current branches working directory.  

### Share & Update

``git remote add [alias] [url]``  
Add a git url as an alias  

``git fetch [alias]``   
Fetch all branches from the git *remote*  

``git merge [alias]/[branch]``  
Merge remote branch onto current branch, bringing it up to date.

``git push [alias] [branch]``  
Upload local branch commits to remote repository branch.  

``git pull``  
*Fetch* then *merge* any commits from the tracking remote branch.  




## Logs

``git log``   
Displays all commits in current working directory.  

``git log --follow [file]``  
Diaplay list of version history including renames for the specified file.  

``git diff [first-branch]...[second-branch]``  
Display the content difference between the two specified branches.

``git show [commit]``  
Displays metadata and content changes kf the specified commit.






## Glossery

### git
An open source, distributed version-control system
### GitHub
A platform for hosting and collaborating on Git repositories
### Commit
A Git object, a snapshot of your entire repository compressed into a SHA
### Clone
A local version of a repository, including all commits and branches
### Branch
A lightweight movable pointer to a commit
### Tag
### HEAD
representing your current working directory, the HEAD pointer can be moved to different branches, tags, or commits 
when using ``git checkout``
### Repo
### remote
A common repository on GitHub that all team member use to exchange their changes
### fork
A copy of a repository on GitHub owned by a different user
### pull request
A place to compare and discuss the differences introduced on a branch with reviews, comments, integrated 
tests, and mor