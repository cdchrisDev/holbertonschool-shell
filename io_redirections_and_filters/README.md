This is the holberton shell repository 

**INPUT AND OUTPUT**

## Print hello world on bash 
0. > echo "Hello world"
## Write a script that displays a confused smiley "(Ôo)'.
1. > echo "\"(Ôo)'"
## Display the content of /etc/passwd
2. > cat /etc/passwd
## Display the content of /etc/passwd and /etc/hosts
3. > cat /etc/passwd /etc/hosts
## Display the last 10 lines of /etc/passwd
4. > tail -10 /etc/passwd
## Display the first 10 lines
5. > head -10 /etc/passwd
## Write a script that displays the third line of the file iacta. Without sed
6. > perl -ne 'print if $. == 3 ' < iacta
## Writing the exact string using scapes characters
7. > echo "Best School" >> "\\*\\\'\"Best School\"\\'\\\*$\?\*\*\*\*\*:)"
## Create a file with content ls -la, if exist rewrite
8. > ls -la >> "ls_cwd_content"
## Duplicate the last line of the file
9. > tail -n 1 iacta >> iacta
