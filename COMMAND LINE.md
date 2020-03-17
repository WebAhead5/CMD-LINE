# COMMAND LINE

# 1 - What is CMD LINE -
The command line, also called the Windows command line, command screen, or text interface, is a user interface that is navigated by typing commands at prompts, instead of using the mouse.  a command line only uses a keyboard to navigate by entering commands and does not utilize a mouse for navigating.
Advantages:
-Much faster. No GUI overhead (unless we are talking pseudo-terminals).

-They don't need memorization. If you forgot a command option, just run it with -h, —help, or man/info it.

-For complex tasks, the command line can be scripted to automate things.

-To run sequence of commands as a single command.

# 2 - Why might you want to customize it?-

- improve your workflow significantly and help you write more code.
- make it looks good.
- tasks more efficient, and even faster.
-----------------------------

# 3 - CMD LINE Custimization

You can customise you CMD Line in a number of ways, including the following:

## Change Prompt (PS1 varible):
- You can change your prompt by altering the PS1 varible in the comand line with the following code

`PS1="new prompt"`


- So `PS1="Jake's Prompt >"`, would result in:

![alt text](https://i.ibb.co/syZGZSW/Prompt.png)

- As an example, `PS1="\w"` makes the prompt the current working directory, for example:


![alt text](https://i.ibb.co/SBSM4PS/directory.png)


- You can also add a bunch of other useful things to the prompt, such as the things listed below. 

![alt text](https://i.ibb.co/c1dx3XP/list.png)

- For example, to add a your user name followed by a working 24hr clock you could simply type `PS1=" \u \T : "`

![alt text](https://i.ibb.co/xCxZ4Bk/time.png)




### Changing Color:
- We can change the color of elements of the terminal, the possible colors and their codes are below.

![alt text](https://i.ibb.co/8zk0V7g/color.png)

-The need to enclose the color in ``\[`` and ``\]`` so that the terminal can read it, so the code for __blue__ will look like this:

`\[\e[34m\]`

- We can then turn elements into that color by including them, for example in the prompt/PS1 as follows:

![alt text](https://i.ibb.co/Sr6tBrw/blue.png)

- To stop everything going the same color, you need to include `\e[00m\]` at the end of the prompt, as follows:

`PS1="\[\e[34m\] BLUE PROMPT ONLY: \e[00m\]"`

![alt text](https://i.ibb.co/gPfXNCr/bluewhite.png)


## Saving your changes to Profile
- The above will only give you temporary changes to the terminal, so in order to make these permanant you need to add them to your **Profile**.


- In order to do this you need to find `.bashrc file` located in your home directory (type `ll` at home screen to view the files, then `code .bashrc` in terminal to open in code editor)

- You then need to `export` the PS1 edit into the Profile file and save it, to ensure eveythime you open the terminal the changes are there:

`export PS1="#####"`

![alt text](https://i.ibb.co/BTd0Mmw/bashedit.png)

### GIT BRANCH
- You can also add your current Git Branch to your command prompt, but this requires including a new function within you **bashrc** file before you are able to run the code. 

- copy and paste the following function into your bashrc file:

`git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}`

- Then this will then allow you to include `\$(git_branch)` is your PS1 export to add the current git hub branch to the prompt (branch is called **"updateStyle"** in this case, and is only active when you are in a folder tracked by GitHub):

`PS1="\[\e[34m\] BLUE PROMPT ONLY: \e[00m\]  \$(git_branch)"`


![alt text](https://i.ibb.co/hdTgshP/bluegit.png)

- Please see following guide for more info: [Link to Git Branch Guide](https://www.shellhacks.com/show-git-branch-terminal-command-prompt/)


# Package Manager

You can also install a **Package Manager**
- A Package manager is 
`Package management is a method of installing and maintaining (which includes updating and probably removing as well) software on the system.`


- This allows you to 
 `To Install Software`

 You can install via:-
### The APT is the tool
Complete command is apt-get and it’s the easiest way to 
install files/Softwares packages.
    

    
    
    
    sudo apt-get install ${packagename}


To remove/uninstall any software, just use remove


    sudo apt-get remove ${packagename}




The software packages are somewhere in the online repositoies, APT handles a local database on the user’s hard drive that contains informations about the available packages and where they are located. 


to get the all newly uploaded packages on the repositories, user need to update APT regularly.
To update APT database:

    sudo apt-get update






link with more info 
https://www.howtogeek.com/63997/how-to-install-programs-in-ubuntu-in-the-command-line/ 




-----------------------------

