# This is the holberton shell repository 

**Basics:**   
	to see display the current directory   
	> pwd     
	To change to `/home`   
	> cd /home      
	Display current directory on long format   
	> ls -l     
	Display current directory including hidden files  
	> ls -la  
	Display **long format, user and groups numerically and hidden files**   
	> ls -la    
	Create a directory called `my_first_directoy` in `/tmp/`  
	> mkdir my_first directoy /tmp/  
	Move the file `betty` from `/tmp/` to `/tmp/my_first_directory`  
	> mv /tmp/betty /tmp/my_first_directory  
	Delete the `betty` file   
	> /tmp/my_first_directory  
	Delete the directory `my_first_directory` in `/tmp/` directory   
	> rm -r /tmp/my_first_directory   
	Changin the working directory to the previous one  
	> cd ..  
	List the current, previous and `/boot` directory  
	> ls -la . .. /boot  
	Print type file named `iamafile` in `/tmp`  
	> file /tmp/iamafile  
	Create a Symbolic link to `/bin/ls` named `__ls__`  
	> ls -s /bin/ls __ls__  
	Copy all html files but just to update or non-existed from the working to the parent directory  
	> cp -R -u *.html ..  
	Move all files starting with uppercase to the `/tmp/u` directory  
	> delete all files in the working directory ending with ~  
	Create directories `welcome/` `welcome/to/` `welcome/to/holberton` one inside another  
	>mkdir -p welcome//to//holberton  
