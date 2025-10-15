# Pondering PATH


## The PATH Variable

### Objective : To learn about path variables in terminal.

Flag : `pwn.college{Eg8k9lr9IXW8D4jSwhHTBKN-0fF.QX2cDM1wCO3EzNzEzW}`

```
PATH=""
/challenge/run
```
### Solution : we first set the value of PATH variable to nothing so that /challenge/run cannot use the rm command to delete the flag.

### What I Learned : shell uses PATH to find the directory of the command needed to be executed.


## Setting PATH

### Objective : To learn how to be run commands directly without writing the path using PATH.

Flag : `pwn.college{szfSGoBitTBxey2cFNRPasMca_G.QX1cjM1wCO3EzNzEzW}`

```
PATH=/challenge/more_commands/
/challenge/run
```
### Solution : we first set the value of PATH to the directory of the win command then run the /challenge/run to get the flag.

### What I Learned : we can use PATH for our convinience as we can run commands directly by adding their path to the PATH variable.


## Finding commands

### Objective : To learn how to find the paths of commands in PATH variable.

Flag : `pwn.college{ExjHrdBeC3BznGwOKyuoSLiU5Fc.01NzEzNxwCO3EzNzEzW}`

```
which win
ls -l /challenge/paths/7443
cat /challenge/paths/7443/flag
```
### Solution : we first search the path to which the win commands belongs to and then find the flag file in the same directory.

### What I Learned : we can find the path of a command in the PATH variable using which command.


## Adding commands

### Objective : To revise about altering path variable.

Flag : `pwn.college{I5K3Yu-9eHMqnilO6hFFPoyMb2W.QX2cjM1wCO3EzNzEzW}`

```
which cat
echo "/run/dojo/bin/cat /flag" > win
chmod ugo+x win
PATH=/home/hacker
/challenge/run
```
### Solution : we find the absolute path of the cat command then set the command to print the flag in the win file then set the directory of the win file in PATH variable and then run /challenge/run to find the flag.

### What I Learned : revision on last modules.


## Hijacking commands

### Objective :

Flag : ``

```

```
### Solution : 

### What I Learned : 