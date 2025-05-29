Linux is the kernel of a family of open-source unix-like Operating system.

What is OS? 
- A system software that manages computer hardware and provides various services for computer programs.

Kernel: is the core part of an OS and responsible for managing the hardware including the CPU, memory and other devices.

## The Command Line:
- echo: this command allow to output the text in the commandline
	- echo -e 'you are \namazing'

The \n is a line breaker here.
## Directory commands: 
---
- The cd commands usages for change directory and pwd for print the current working directory: 
	- Cd / -- you will go to root directory
	- Cd .. -- you will move to parent directory 
	- Cd ../.. two level up from the directory you're in
- pwd will print the current directory you are in 
## Listing the content
---
- ls -t this will sort the directory by time
- ls -r -t it will reverse the order
- ls --colours=never it will remove all the colours(always, never, auto).
- ls -a display all the files.
- ls / this argument will work as a path.
## Absolute vs relative path
---
- These paths starts with a "/" and defines a complete path to a file and works anywhere no matter our current working directory.
	- Ex: /home/Desktop/studies
- if i type cd ~/desktop/ this also define the absolute path and it will take me to the path i gave.
---
- The relative path will be resolved to the current working directory we are in.
	- if i type ./Desktop so you will be in the desktop folder.
	- when you type ../Desktop it will level up in the directory.
	- it will not work directly from the root, you have to give a absolute path in the first place.

## Executing Multiple Commands
---
- TO do this we have to add a **;(semicolon)** between the commands to run.
	- command1; command2;
- Ex: echo -n hello; echo world
- **like cd ..; cd Desktop; ls** this will first go a level up in the directory and then it will go to desktop and list all the content.
## How to get help
---
- --help/ -h so we can use this program for any command line tool that exist.
- **Man** command open the manual for the command line tools and this must be installed on the system.
	- in this just install **sudo apt install man-db**.
## User Management
---
- **System accounts:** These are responsible for running background tasks such as webserver, database and they don't have a home directory.
- **Regular accounts:** These accounts will have their own files and directories and can not perform admin tasks.
- **Superuser(root):** The root user has unrestricted access to the entire system including the files and directories of a normal users.
	- the user can do anything rather than admin tasks without any restrictions.
## Elevating Privileges: sudo
---
- To get the temporary admin privileges put the **sudo** with any command and you're good to go.
	- Ex: **sudo ls /root** now the normal user can access the root directory without any root privileges on a temp bases and when the user cut the terminal window then will back to normal privileges. 
- Be careful with command when you have the root privileges
	- **sudo rm -rf /etc** this command will destroy the installed distro on the system.
## Package Management Linux
---
- The linux distros have a centralized way to install software and this process called the package management.
- on the debian based distros use the tool **apt** to get the updates.
	- **apt update** this will update the packages but we have to have admin privileges so
		- **sudo apt update**
		- **sudo apt upgrade** this will upgrade the packages
		- **sudo apt full-upgrade or sudo apt dist-upgrade** this will upgrade whole os within the system.
		- **sudo apt install** [packagename] to install the specific tool or package.
		- **sudo apt remove** [packagename] to remove the specific tool or package.
		- **sudo apt autoremove** this command will remove those packages those are no longer needed.
- **Cowsay:** just a small command line tool for fun.