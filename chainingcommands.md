# Chaining Commands


## Chaining with semicolons

### Objective : To learn how to chain commands.

Flag : `pwn.college{g2hQBAO6ugb4ONlL5pA3C-0EJJM.QX1UDO0wCO3EzNzEzW}`

```
/challenge/pwn ;/challenge/college
```
### Solution : we chain the commands with ; to get the flag.

### What I Learned : we can chain commands using ; in terminal.


## Building in Success

### Objective : To learn how to chain commands only if the first command succeceeds.

Flag : `pwn.college{c6rGqmtrQ_W5pMzJojPRAECxbBn.0lM0MDOxwCO3EzNzEzW}`

```
/challenge/first-success && /challenge/second
```
### Solution : we chain the commands using && so that the second one works only if the first one executes successfully.

### What I Learned : we use && command to chain two commands where the second command only runs if the first command executes successfully.


## Handling Failure

### Objective : To learn how to chain commands using the or command in terminal.

Flag : `pwn.college{si5ETFXv1eF9L9fZxA98O8ePWi4.01M0MDOxwCO3EzNzEzW}`

```
/challenge/first-failure || /challenge/second
```
### Solution : we link the first and second command with || to find the flag.       

### What I Learned : we can chain two commands with || operator so that the second command only runs if the first command fails.


## Your first shell script

### Objective : To learn about shell script.

Flag : `pwn.college{geHGV-9zLW_GvkCfTR7cXWFpHNz.QXxcDO0wCO3EzNzEzW}`

```
touch x.sh
nano x.sh
(/challenge/pwn
/chalenge/college)
bash x.sh
```
### Solution : we put both the commands in x.sh file and then run the file with bash to get the flag.

### What I Learned : we use .sh files as shell scripts and we can run them with bash commmand in terminal.


## Redirecting script output

### Objective : 

Flag : `pwn.college{4L7LU9RCzmyj0rKWX6xxA_dgQ4M.QX4ETO0wCO3EzNzEzW}`

```
touch new.sh
nano new.sh
(/challenge/pwn
/chalenge/college)
bash new.sh | /challenge/solve
```
### Solution : we create the shell script and then pipe the output to the /challenge/solve.

### What I Learned : how we can redirect the output of many commands with putting them in a shell script and piping the output to another command.


## Executable shell scripts

### Objective : To learn how we can run shell script without invoking the bash command.

Flag : `pwn.college{I2IP6oGzCV3g1CQjFgZPDwP8PY5.QX0cjM1wCO3EzNzEzW}`

```
touch lol.sh
nano lol.sh
(/challenge/solve)
chmod u+x lol.sh
./lol.sh
```
### Solution : we make a new shell script and then change its permission to give user access to execute the file and then we execute the file to find the flag.

### What I Learned : we can make the shell scripts in executables and then execute them to run the script.


## Understanding Shebangs

### Objective : To learn about shebangs.

Flag : `pwn.college{8bXin7j2hSWd-XnGpDtiZbeLUKH.0VOzMDOxwCO3EzNzEzW}`

```
touch /home/hacker/solve.sh
nano /home/hacker/solve.sh
(#!/bin/bash
echo "hack the planet")
chmod u+x /home/hacker/solve.sh
/challenge/run
```
### Solution : we make the new shell script and then to add the shebang to it and then give the user execution permission of the file and then run /challenge/run to get the flag.

### What I Learned : shebangs are used by the linux kernel to determine the interpreter path to run the file.


## Scripting with Arguments

### Objective : 

Flag : `pwn.college{8sp00L59Lsf2XI8dCvTWOXzvedF.0VNzMDOxwCO3EzNzEzW}`

```
nano /home/hacker/solve.sh
(#!/bin/bash
echo "$2 $1")
/challenge/run
```
### Solution : we first make a shell script where i interchange two order of the two inputs and then run /challenge/run to get the flag.

### What I Learned : how we can give arguments to shell scripts in terminal.


## Scripting with Conditionals

### Objective : To learn if statements in shell scripts.

Flag : `pwn.college{MQwSNgembRCH87VMzKdbyVPXmwq.0lNzMDOxwCO3EzNzEzW}`

```
nano /home/hacker/solve.sh
(#!/bin/bash
if [ "$1" == "pwn" ]
then
    echo "college"
fi )
/challenge/run
```
### Solution : we used if statement in the shell script to check weather the input argument was pwn if yes then it would print college else nothing.

### What I Learned : usage and syntax of if statement in shell scripts.


## Scripting with Default cases

### Objective : To learn how to use else in the if statements in shell script.

Flag : `pwn.college{IjC8KjqFm9aRWoDeuDS5sEZnVRT.01NzMDOxwCO3EzNzEzW}`

```
nano /home/hacker/solve.sh
(#!/bin/bash
if [ "$1" == "pwn" ]
then
    echo "college"
else
    echo "nope"
fi )
/challenge/run
```
### Solution : we add an else statement to the previous if statement which will run if the input is not pwn.

### What I Learned : usage and syntax of else in shell script.


## Scripting with Mulitple Conditions

### Objective : To learn else if statement in shell script.

Flag : `pwn.college{sVs7qfgxeggAUMJ0Ge7tLk2I9wO.0FOzMDOxwCO3EzNzEzW}`

```
nano /home/hacker/solve.sh
(#!/bin/bash

if [ "$1" == "pwn" ]
then
        echo "college"
elif [ "$1" == "hack" ]
then
        echo "the planet"
elif [ "$1" == "learn" ]
then
        echo "linux"
else
        echo "unknown"
fi)
/challenge/run
```
### Solution : we use if, elif and else statements according to given conditions to obtain the flag.

### What I Learned : usage and sytax of elif statement in shell script.


## Reading shell scripts

### Objective : To revise the topic of shell scripts.

Flag : `pwn.college{0ZJgB-mkew4r0J-DK-K5ZS-bvoA.0lMwgDOxwCO3EzNzEzW}`

```
cat /challenge/run
/challenge/run
(hack the PLANET)
```
### Solution : we first read the /challenge/run file and find out that the correct argument was "hack the PLANET" and then we run it and pass the correct argument to it to obtain the flag.

### What I Learned : to read file contents to find hidden clues.