# Pondering Paths

## Challenge : The Root

### Objective : To learn about absolute paths in a command line interface (shell).

Flag : `pwn.college{E-PNNZmimEXlW9f8UneStJObzv3.QX4cTO0wCO3EzNzEzW}`

```
/pwn
```

## Program and Absolute Paths

### Objective: To dive deeper into the concept of absolute paths and executing programs.

Flag : `pwn.college{QAxkXOmL0T2lGGoW_lWJ1xqgsM2.QX1QTN0wCO3EzNzEzW}`

```
/challenge/run
```

## Position thy Self

### Objective : To learn about navigating through directories and executing programs from absolute paths.

Flag : `pwn.college{oo-oOupDLkFYpC_6FrUS9LBaI4x.QX2QTN0wCO3EzNzEzW}`

```
/challenge/run
cd /var/log
/challenge/run
```
### Solution : First I tried to run the program, then it provided me the correct directory in which I should run the program again. So, I navigated to that directory and executed the program.

### What I Learned : cd command is used to navigate through directories.


## Position Elsewhere

### Objective : To learn about navigating through directories and executing programs from absolute paths.

Flag : `pwn.college{A3eyxaj2VGckBAplJZ-IIQrw1fT.QX3QTN0wCO3EzNzEzW}`

```
/challenge/run
cd /proc/139/fd
/challenge/run
```
### Solution : To first change directory and then run the program to obtain the flag.

## Position yet elsewhere

### Objective : To run program from a specific path.

Flag : `pwn.college{YL3vFMWI-Qh5D-GKiAPp782nmMr.QX4QTN0wCO3EzNzEzW}`

```
/challenge/run
cd /sys
/challenge/run
```
### Solution : to first go to a different directory to run command in absolute path.

### What I Learned : absolute paths can be called from anywhere .


history | cut -c 8-

## Implicit relative paths, from /

### Objective : To run program from a relative path while being in / directory.

Flag : `pwn.college{Axn5P4jTzOrzBY4JYx4f1mNappU.QX5QTN0wCO3EzNzEzW}`

```
/challenge/run
cd /
challenge/run
history | cut -c 8
```
### Solution : First we have to go to / directory to call challenge/run as a relative path not and absolute path.

### What I Learned : about relative paths.


## Explicit relative paths, from /

### Objective : to learn about '.' in usage with respect to relative paths.

Flag : `pwn.college{Y4x4dpAfLHyUvHcGKLywseFgZo5.QXwUTN0wCO3EzNzEzW}`

```
cd /
./challenge/run
```
### Solution : first we got to / directory and then run the program by calling the relative path using '.'.

### What I Learned : relative paths can also be called using . in front .


## Implicit relative path

### Objective : to explitily use relative path to launch program .

Flag : `pwn.college{4CjtcZOUzjIBxMca0J7ZA9beW1H.QXxUTN0wCO3EzNzEzW}`

```
/challenge/run
cd /proc/139/fd
/challenge/run
```
### Solution : first we cd into the challenge directory and then launch program using relative path.

### What I Learned : the difference between naked and explicit path.


## home sweet home

### Objective : To make use of ~ shortcut.

Flag : `pwn.college{Yyc0CTCplEwkkejZtKK7Yx0jQEr.QXzMDO0wCO3EzNzEzW}`

```
/challenge/run ~/a
```
### Solution : call the absolute path and pass ~/a as argument to solve the challenge.

### What I Learned : the ~ shortcut.