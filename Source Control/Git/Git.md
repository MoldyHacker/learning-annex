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



