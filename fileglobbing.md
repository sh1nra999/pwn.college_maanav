# File Globbing


## Matching with *

### Objective : To learn about globbing

Flag : `pwn.college{4gX2E9_WfCb9rQ-3WwIgkAC7IX0.QXxIDO0wCO3EzNzEzW}`

```
cd /c*e
/challenge/run
```
### Solution : we first cd into /challenge directory by globbing and then run the flag program.

### What I Learned : how globbing is used in different situations.


## Matching with ?

### Objective : To learn about how to use '?'.

Flag : `pwn.college{QwF89-aJCpwxGlB9SUBL0zSa-h7.QXyIDO0wCO3EzNzEzW}`

```
cd /?ha??enge
/challenge/run
```
### Solution : we first cd in challenge directory using ? instead of c and l and the run the flag program.

### What I Learned : '?' can be used to replace a single charachter.


## Matching with []

### Objective : To learn how to glob using [].

Flag : `pwn.college{ksWCODumbVwu_28AqFWcxqU3Gzb.QXzIDO0wCO3EzNzEzW}`

```
cd /challenge/files
/challenge/run file_[bash]
```
### Solution : we first cd into /challenge/files and then run the program with the arguments to run the multiple files using [] globbing.

### What I Learned : we can use restricted globbing using [].


## Matching path with []

### Objective : To learn how to use [] globbing in paths.

Flag : `pwn.college{QFgNIv_i9sqJONuQq7iWwC5eZVW.QX0IDO0wCO3EzNzEzW}`

```
/challenge/run /challenge/files/file_[bash]
```
### Solution : we find the flag using [] globbing with flag_[bash] with paths.

### What I Learned : we can use [] globbing with paths.


## Multiple globs

### Objective : How to use double * for multiple globs.

Flag : `pwn.college{IEey7Wm4Q34K_yeM4-ZoLc-pN9Y.0lM3kjNxwCO3EzNzEzW}`

```
cd /challenge/files
/challenge/run *p*
```
### Solution : first we cd into /challenge/files and then run /challenge/run and as the argument we use the double * globbing to pass every file containing p.

### What I Learned : we can use double * the glob multiple files containing the same pattern.


## Mixing globs

### Objective : to learn how to use globs with diversely named files.

Flag : `pwn.college{Ihrlwqt7q_1o6vO225a9qOf7roj.QX1IDO0wCO3EzNzEzW}`

```
cd /challenge/files
/challenge/run [cep]*
```
### Solution : we first cd in /challenge/files and then we run the program with the argument with [cep]*.

### What I Learned : we can use restriced globbing with * globbing.


## Exclusionary globbing

### Objective : to learn how to use inverse [] globbing.

Flag : `pwn.college{AS7TxU8mNwjkSGElPHdnr_dO_oz.QX2IDO0wCO3EzNzEzW}`

```
cd /challege/files
/challenge/run [!pwn]*
```
### Solution : we use the argument [!pwn]* to use files which do not start with p, w or n.

### What I Learned : we can use ! at the start of [] to inverse the globbing to exlude those letters.


## Tab completion

### Objective : To learn how to use tab completion in terminal

Flag : `pwn.college{sbxy1cOteBhxvGa_5eXYJNR9Rjk.0FN0EzNxwCO3EzNzEzW}`

```
cat /challenge/pwncollege
```
### Solution : we use tab completion to auto write pwncollege.

### What I Learned : we can use tab completion to auto write things present in the directory.


## Multiple options for tab completion

### Objective : To learn how tab completion works when there are multiple possibilities.

Flag : `pwn.college{gatx-ihUaT6YzguBTRXT0TIySkF.0lN0EzNxwCO3EzNzEzW}`

```
cat /challenge/files/pwn
cat /challenge/files/pwncollege-f
cat /challenge/files/pwncollege-flag   
```
### Solution : we use the cat with /challenge/files/p to auto complete with tab completion to find the flag file.

### What I Learned : i learned that if there are multiple possibilities for auto completion then with second tab click it shows all the possiblities.


## Tab completion on commands

### Objective : To learn about tab completion on commands

Flag : `pwn.college{ENJjg3k4zf5409RiEKqpP_XKup2.0VN0EzNxwCO3EzNzEzW}`

```
pwncollege-26840
```
### Solution : we type pwncollege and then use tab completion to complete the command to find the flag.

### What I Learned : tab completion can be used for commands also.