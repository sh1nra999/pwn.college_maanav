# Shell Variables


## Printing Variables

### Objective : To leran about variables in terminal.

Flag : `pwn.college{EwQY7bczsxHuYWJBo2i_hvkEfEa.QX3UTN0wCO3EzNzEzW}`

```
echo $FLAG
```
### Solution : we needed to echo the variable FLAG in the terminal.

### What I Learned : how to print variables in terminal.


## Setting Variables

### Objective : To learn how to set variables in terminal.

Flag : `pwn.college{c0WJtful1OQ5piaZqlNCTW3iOeX.QX5UTN0wCO3EzNzEzW}`

```
PWN=COLLEGE
```
### Solution : we gave the value of COLLEGE to variable PWN using =.

### What I Learned : how to assign vairables value in terminal and how to call them.


## Multi-word variable

### Objective : To learn how to assign multi word value to variables.

Flag : `pwn.college{YcInepFTi23Bkv1hIavKUH_flj3.QXwYTN0wCO3EzNzEzW}`

```
PWN="COLLEGE YEAH"
```
### Solution : i assignes the value COLLEGE YEAH to PWN using "".

### What I Learned : we can assign multi word value to a variable using "" in terminal.


## Exporting variables

### Objective : To learn how to use variables outside local environment.

Flag : `pwn.college{klOnMXvawy94xJDP3oGJqysQfUd.QXyYTN0wCO3EzNzEzW}`

```
export PWN=COLLEGE
COLLEGE=PWN
/challenge/run
```
### Solution : we first set the PWN variale to COLLEGE variable and exported it and then set the value of the variable COLLEGE to PWN but not exported it.

### What I Learned : we can use export to the variable to use it outside the local environment.


## Printing exported variables

### Objective : To learn how to print all exported variables in terminal.

Flag : `pwn.college{0_4_nFNAqzd6bV1JiT1IEY97GgV.QX4UTN0wCO3EzNzEzW}`

```
env
```
### Solution : we types the env to print all the exported variables and search for the flag through them.

### What I Learned : env command can be used to print all the exported variables.


## Storing Command Output

### Objective : To learn how to store output of a command in a variable in terminal.

Flag : `pwn.college{E5xdIAFNABZeJABtgAWPEy7ck9Q.QX1cDN1wCO3EzNzEzW}`

```
PWN=$(/challenge/run)
echo $PWN
```
### Solution : we first the store the output of /challenge/run to the variable PWN and then echo the variable PWN to find the flag.

### What I Learned : we can store the output of a command in a variable using $().


## Reading Input

### Objective : To learn how to get input from the user in terminal.

Flag : `pwn.college{I2J1AIBr0-yY01sd9t-okARDaIf.QX4cTN0wCO3EzNzEzW}`

```
read -p "enter value : " PWN
enter value : COLLEGE
```
### Solution : we first inputed the value of PWN from the user as COLLEGE to get the flag.

### What I Learned : we can use read to input data from the user in terminal.


## Reading files

### Objective : To learn how to redirect a file and input for a variable in terminal.

Flag : `pwn.college{weHNHeingYsWUUNbO1yw4qE5GwO.QXwIDO0wCO3EzNzEzW}`

```
read PWN < /challenge/read_me
```
### Solution : we redirected the output of /challenge/read_me into the input of PWN variable to get the flag.

### What I Learned : we learned how to redirect output of a program to input of a variable in terminal.