## A beginner's guide to the command line


 Have you seen those 🕵️‍♂️ hackers hacking systems in sci-fi movies? Isn't it cool? It's usually a computer genius typing on the blank screen(actually terminal), a lot of binary numbers, green text, and other cool stuff.  I remember I used to impress my friends just by using the terminal in front of them. 


![terminal.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1594889231572/Vj3pgPu-O.png)


😂 Well, we are not going to discuss hacking here. Sorry, I know. 

We will be discussing the superpowers of using the command line, why you should learn how to use it, some basic commands you should know, and some more interesting stuff. Let's get started.

![giphy (1).gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1593190717812/9bbfmLu8e.gif)

## What is the command-line interface?
Command-line Interface (CLI) 💻 is a text-based interface used to interact with software and operating system by typing commands into the interface and receive a response in the same way. 

It is a program that allows users to type text commands instructing the computer to do specific tasks. The command-line interface is the original way of talking to our machine. Don't get confused with the terms command line and terminal. They are often used interchangeably to indicate a text-based interface for navigating your operating system. Command-line is very windows centric terminology, whereas the terminal is very mac centric.

> 
If you have Windows installed in your system, I would suggest using [Git bash](https://gitforwindows.org/) instead of the default command prompt. 

It allows you to use Unix/Linux commands on a Windows computer. Also, you can customize it as you want or choose different themes and all. I am using the 🧛‍♂️ [Dracula theme](https://draculatheme.com/) and I am loving it. Try it and thank me later.

## Command line vs. GUI

![GUIvscli.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1595223958808/t___moFkz.png)

GUI stands for Graphical User Interface whereas CLI stands for Command Line Interface. There is a huge debate among developers on GUI vs CLI.  GUI is visually intuitive. I know. And beginners tend to learn how to use a GUI faster than a CLI as it is more user-friendly.  There is certainly nothing wrong with using GUIs.

%[https://twitter.com/bendhalpern/status/1067602747191689224]


But once you overcome the beginner phase and understand the potential of the command line interface, you will start appreciating how CLI makes your work easy and efficient at the same time.

## Why you should learn the command line?

We don't just use the command line because it's cool. Using a command line, you can perform almost all the same tasks that can be done with a GUI. Also, it is faster than the GUI, uses fewer resources, and gives more control of what you're doing.
 
As a developer, we most likely use the command line for

### 📌 Using git on the command line
The command line is the only place you can run all Git commands as most of the GUIs implement only a partial subset of Git functionality for simplicity. And you’ll eventually need to use Git through the command line for advanced tasks.

For example, if you need to fix complex merge conflicts, rebase branches, merge manually, or undo and roll back commits, you’ll need to use Git from the command line and then push your changes to the remote server.

```
git push origin master
``` 
### 📌 Executing your code
You can compile and execute your code on the command line.
For example, To run a Python script store in a ‘.py’ file in the command line, we have to write ‘python’ keyword before the file name in the command prompt.

```
python hello.py

``` 

### 📌 Installing npm packages and libraries
There will be many situations where you have to use only CLI. For instance, you need some node modules.  As npm is a command-line package manager for Node, you have to use the command line to install it like

```
npm install whatever-thing

``` 
NPM does not have a GUI. Every package has to be installed via npm command.
### 📌 starting up a server
If you are using some framework or library or creating something with frontend as well as backend, You will need a command line to start a server.
For example, while using create-react-app we need to do

```
npm start
``` 


- and more.

## 📕 Basic commands you should know
There are hundreds of different commands that can be used in a command line. And we will be discussing a few of them.
> 
 **Note**: I am using Git bash, so we will use Unix/Linux commands here. Although I will share the equivalent windows command too. 


### pwd
pwd prints the name of the working directory, a directory or folder in which you are currently in. Right now I am in a folder named dev. So it will print the complete path of the dev folder.

![1 pwd.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595178354078/wqCBWO_mp.gif)

### List all files
ls command is used to display the list of all files and subdirectories contained in a specific directory. For windows, dir command does the same.


![new ls.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595211608629/YQ517oKKa.gif)


![Screenshot (311).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1595211713887/CKb8bNLDb.png)

### Change directory
cd command is known as change directory command. It is used to change the current directory. The syntax is [ cd directory_name ]. For windows, it's the same command.



![cd app.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595212126297/jIailIm7z.gif)

Here I changed to the app directory. You can check using pwd command. It will give the path of a new directory now. i.e.  /c/Users/Rutik/Desktop/dev/app

### Move to the parent directory
There is another version of the cd command. cd .. command is used to move to the parent directory of the current directory, or the directory one level up from the current directory. “..” represents parent directory.


![4 parent.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595210408741/jpbJKDg3q.gif)

So now I am back at the parent directory of app folder. i.e. /c/Users/Rutik/Desktop/dev

### Creating a new folder 
The mkdir command allows us to create or make new directories. mkdir stands for “make directory". The syntax is [ mkdir folder_name ]. 
For windows, it's [ md folder_name ] command.

![new folder.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595212793838/q-E595E6M.gif)
Here we created a new folder named icons in the dev folder.

![Screenshot (313).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1595212929406/RlaC-aQXc.png)

### Creating a new file
touch command is used to create a file without any content. The file created using touch command is empty. The syntax is [ touch file_name ]. For windows, the command is a bit different. Its [copy nul file_name].

![new touch.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595214062977/Yt2fnbq5S.gif)

We created a new index.html file in the dev folder.

![Screenshot (315).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1595214175736/KDV87ybCn.png)

### Open file in browser
To open a file in the browser we simply use the start command. It's syntax is [ start file_name ]. For windows, it's the same command.  Depending on the file type, it will open in the respective program. Here It will open index.html file in the default browser.


![start start.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595217011884/ygrOc9TGG.gif)


### Deleting a file
The rm command is used to delete files. rm stands for remove. The syntax is [ rm file_name].  Once you delete the file then you cannot recover the contents of files and directories. For windows, the command is [ del file_name ].


![new rm.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595218949868/Mz-TpHJak.gif)
And it's gone. index.html file is deleted from the dev folder.
![Screenshot (313).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1595212929406/RlaC-aQXc.png)

### Deleting a folder
Normally, rm wouldn’t delete the directories but when used with -r option, it will delete. -r stands for recursive. It will delete all the files and sub-directories recursively of the parent directory. The syntax is [rm -r folder_name ]. For windows, it's [rmdir folder_name ].


![remove f.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595219983530/KamPf_kSh.gif)

![Screenshot (311).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1595211713887/CKb8bNLDb.png)

### Clear screen
clear command is used to clear the terminal screen. It doesn’t take any argument.
For windows, the command is [ cls ].

![clear screen.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595220871429/FBjSI7UXS.gif)

### Use of tab
The use of tab will help you speed up typing commands. Just hit Tab while typing a command, option, or file name and the command line will automatically complete what you're typing or suggest options to you.

![use tab.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595221590044/Yt_ntxuIX.gif)

### Using up and down arrow keys
Using the up and down arrow keys, you can recall previously-entered commands to the command line.

![use arrow.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595222058193/nYUXp1zLe.gif)


### Running a program
You can Run a Program on Command line using the start command. 

![notepad.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1595011821301/qyq8IsIYt.gif)

The program's name must be the file's system name, not its shortcut name (for example, Command Prompt's system name is cmd). 
Common program names are 
- Notepad - notepad
- Paint - mspaint
- Task Manager - taskmgr
- File Explorer - explorer

## Conclusion
Believe it or not, but using the command line gives you 🦸‍♂️superpowers. There are far more things that we can do using the command line. So, learning the command line will surely give you an advantage. So try exploring it.  

I keep writing about the things I learned and applied. So you can connect with me on [Twitter](https://twitter.com/WankhadeRutik), [Github](https://github.com/rutikwankhade)  or [Linkedin](https://www.linkedin.com/in/rutik-wankhade). Also, subscribe to my newsletter and stay up-to-date with my latest blog posts.

⚡ Happy learning!

