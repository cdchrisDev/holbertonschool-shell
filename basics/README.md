# Shell - Basics
## Learning Objectives
### General
* What does RTFM mean?
	* Read The F manual
* What is a Shebang
	* Character sequence at the beggining of a script
### What is the Shell
* What is the shell
	* The shell is a way to comunicate to the computer using commands
* What is the difference between a terminal and a shell
	* Terminal applications are typically text-based and do not have graphical user interfaces.
* What is a shell prompt
	* A command prompt is the input field in a text-based user interface screen for an operating system (OS) or program.
* How to use the history
	* history

# Basics:

## to see display the current directory   
0. > pwd     
## To change to `/home`   
1. > cd /home      
## Display current directory on long format   
2. > ls -l     
## Display current directory including hidden files  
3. > ls -la  
## Display **long format, user and groups numerically and hidden files**   
4. > ls -la    
## Create a directory called `my_first_directoy` in `/tmp/`  
5. > mkdir my_first directoy /tmp/  
## Move the file `betty` from `/tmp/` to `/tmp/my_first_directory`  
6. > mv /tmp/betty /tmp/my_first_directory  
## Delete the `betty` file   
7. > /tmp/my_first_directory  
## Delete the directory `my_first_directory` in `/tmp/` directory   
8. > rm -r /tmp/my_first_directory   
## Changin the working directory to the previous one  
9. > cd ..  
## List the current, previous and `/boot` directory  
10. > ls -la . .. /boot  
## Print type file named `iamafile` in `/tmp`  
11. > file /tmp/iamafile  
## Create a Symbolic link to `/bin/ls` named `__ls__`  
12. > ls -s /bin/ls __ls__  
## Copy all html files but just to update or non-existed from the working to the parent directory  
13. > cp -R -u *.html ..  
## Move all files starting with uppercase to the `/tmp/u` directory  
14. > delete all files in the working directory ending with ~  
## Create directories `welcome/` `welcome/to/` `welcome/to/holberton` one inside another  
15. >mkdir -p welcome//to//holberton  
