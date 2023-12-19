# This is the Holberton-Shell permissions project
## Resources
* [permissions](https://linuxcommand.org/lc3_lts0090.php)

# Permissions
## 1. create a script that switches the current user to the user `betty`
* You should use exactly 8 characters for your command (+1 character for the new line)
* You can assume that the user betty will exist when we will run your script
```
#!/bin/bash
su betty
```

2. > Write a script that prints the effective username of the current user.

´´´
#!/bin/bash
whoami
´´´

3. > Write a script that prints all the groups the current user is part of.

´´´
#!/bin/bash
id -Gn
´´´

4. > Write a script that changes the owner of the file hello to the user betty.

´´´
#!/bin/bash
chown betty hello 
´´´

5. > Write a script that creates an empty file called hello.

´´´
#!/bin/bash
touch hello 
´´´

6. > Write a script that adds execute permission to the owner of the file hello.

´´´
#!/bin/bash
chmod u+x hello
´´´

7. > Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.
* The file hello will be in the working directory

´´´
#!/bin/bash
chmod ug+x,o+r hello
´´´

8. > Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello
* The file hello will be in the working directory
* You are not allowed to use commas for this script

´´´
#!/bin/bash
chmod ugo+x hello 
´´´

9. > Write a script that sets the permission to the file hello as follows:
* Owner: no permission at all
* Group: no permission at all
* Other users: all the permissions
**The file hello will be in the working directory You are not allowed to use commas for this script**

´´´
#!/bin/bash
chmod 007 hello 
´´´

9. > Write a script that sets the mode of the file ´hello´ to this:
´-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello´
* The file ´hello´ will be in the working directory
* You are not allowed to use commas for this script

´´´
#!/bin/bash
chmod 753 hello

´´´
10. > Write a script that sets the mode of the file hello the same as olleh’s mode.
<br />
* The file ´hello´ will be in the working directory
* The file ´olleh´ will be in the working directory

´´´
#!/bin/bash
chmod --reference=olleh hello 
´´´

11. > Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.

´´´
#!/bin/bash
find . -type d -exec chmod a+x {} +
´´´

12. > Create a script that creates a directory called ´my_dir´ with permissions 751 in the working directory.

´´´
#!/bin/bash
mkdir -m 751 my_dir
´´´

13. > Write a script that changes the group owner to ´school´ for the file ´hello´
<br />
* The file ´hello´ will be in the working directory

´´´
#!/bin/bash
chgrp school hello
´´´

14. > Write a script that changes the owner to ´vincent´ and the group owner to ´staff´ for all the files and directories in the working directory.
<br />

´´´
#!/bin/bash
chown --recursive vincent:staff ./*
´´´

15. > Write a script that changes the owner and the group owner of ´_hello´ to ´vincent´ and ´staff´ respectively.
<br />
The file ´_hello´ is in the working directory
The file ´_hello´ is a symbolic link

´´´
#!/bin/bash
chown -h vincent:staff ./_hello
´´´
<br />

16. > Write a script that changes the owner of the file ´hello´ to ´vincent´ only if it is owned by the user ´guillaume´.
<br />
* The file ´hello´ will be in the working directory

´´´
#!/bin/bash
chown vincent --from=guillaume hello
´´´
