# Shell - Init files, variables and expansions
## Resources
* [Expansions](https://linuxcommand.org/lc3_lts0080.php)
* [Shell Arithmetic](https://www.gnu.org/software/bash/manual/html_node/Shell-Arithmetic.html)
* [Variables](https://tldp.org/LDP/Bash-Beginners-Guide/html/sect_03_02.html)
* [Shell initialization files](https://tldp.org/LDP/Bash-Beginners-Guide/html/sect_03_01.html)
* [The alias Command](https://www.linfo.org/alias.html)
* [Technical Writing](https://s3.eu-west-3.amazonaws.com/hbtn.intranet/uploads/misc/2021/6/9112669886fd446a2aa3113c31319d1f468dc160.pdf?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4MYA5JM5DUTZGMZG%2F20231220%2Feu-west-3%2Fs3%2Faws4_request&X-Amz-Date=20231220T002555Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=cfc013c67dbadec5f17bc2be30edda8c461d33b56e17112a5a962bd90869cb70)
## General
* What are the `/etc/profile` file an the `/etc/profie.d` directory
	*  is a directory containing additional scripts that are sourced, or run, by the “/etc/profile” file upon login or new shell start.
* What is the `~/.bashrc` file
	* is a configuration file for the Bash shell. The file consists of commands, functions, aliases, and scripts that execute every time a Bash session starts on Linux or macOS.

# Task
## 0. Create a script that creates an alias.
* Name: `ls`
* Value: `rm *`
```
#!/bin/bash
alias ls='rm *'
```
## 1. Create a script prints `hello user`, where user is the current Linux user.
```
#!/bin/bash
echo "hello $USER"
```
## 2. Add `/action` to the `PATH`. `/action` Should be the last directory the shell looks into when looking for a program.
```
#!/bin/bash
PATH=$PATH:/action
```
## 3. Create a script that counts the number of directories in the `PATH`.
```
#!/bin/bash
echo $PATH | ls | wc -l
```
## 4. Create a script that lists environment variables
```
#!/bin/bash
printenv
```
## 5. Create a script that lists all local variables and enviroment variables, and functions.
```
#!/bin/bash
set
```
## 6. Create a script that creates a new local variable
* Name: `BEST`
* Value: `School`
```
#!/bin/bash
BEST="School"
```
## 7. Create a script that creates a new global variable.
* Name: `BEST`
* Value: `School`
```
#!/bin/bash
export BEST="School"
```
## 8. Write a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.
```
#!/bin/bash
echo $((128 + TRUEKNOWLEDGE))
```
## 9. Write a script that prints the result of `POWER` divided by `DIVIDE`, followed by a new line.
* `POWER` and `DIVIDE` are environment variables
```
#!/bin/bash
echo $((POWER / DIVIDE))
```
## 10. Write a script that displays the result of `BREATH` to the power `LOVE`
* `BREATH` and `LOVE` are environment variables
* The script should display the result, followed by a new line
```
#!/bin/bash
echo $((BREATH**LOVE))
```
## 11. Write a script that converts a number from base 2 to base 10
* The number in base 2 is stored in the enviroment variable `BINARY`
* The script should display the number in base 10, followed by new line
```
#!/bin/bash
echo $((2#$BINARY))
```
## 12. Create a script that prints all possible combinations of two letters, except `oo`.
* Letters are lower cases, from `a` to `z`
* One combination per line
* The output should be alpha ordered, starting with `aa`
* Do not print `oo`
* Your script file should contain maximun 64 characters
```
#!/bin/bash
echo {a..z}{a..z} | tr " " "\n" | egrep -v "oo"
```
## 13. Write a script that prints a number with two decimal places, followed by a new line.
* The number will be stored in the enviroment variable `NUM`
```
#!/bin/bash
printf "%.2f\n" $NUM
```
## 14. Write a script that converts a number from base 10 to base 16.
* The number in base 10 is stored in the enviroment variable `DECIMAL`
* The script should display the number in base 16, followed by a new line
```
#!/bin/bash
printf '%x\n' $DECIMAL
```

