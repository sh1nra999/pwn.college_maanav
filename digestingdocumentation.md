# Digesting Documentation

## Learning from Documentation

### Objective : using proper arguments for running programs

Flag : `pwn.college{QQlYi46kSpTG5wjwIMS1Xvsz77H.QX0ITO0wCO3EzNzEzW}`

```
/challenge/challenge --giveflag
```
### Solution : we needed to call the program using the --giveflag argument

### What I Learned : reading documentation of programs


## Learning complex usage

### Objective : understaing arguments in terminal

Flag : `pwn.college{oGWjMIZlIhyi_fXQKvf8zGDGBWI.QX1ITO0wCO3EzNzEzW}`

```
/challenge/challenge --printfile /flag
```
### Solution : we needed to pass the /flag argument to the --printfile argument of the program

### What I Learned : we can have a argument take in a argument as input


## Reading manuals

### Objective : to learn how to read manuals of commands

Flag : `pwn.college{Igbjmmy8-xjk1iSFM4pB-8Ph1Tj.QX0EDO0wCO3EzNzEzW}`

```
man challenge
/challenge/challenge --gbjmmy 814
```
### Solution : we first read the manual of the challenge command and then find that we need to pass 814 as argument for --gbjmmy to find the flag

### What I Learned : how to use the man command to print the manual for a command


## Searching Manuals

### Objective : we can search a manual

Flag : `pwn.college{YPPYj49pwPdBwEQRFcIcngLXF8-.QX1EDO0wCO3EzNzEzW}`

```
man challenge
/challenge/challenge --ztkee
```
### Solution : we first open the manual of the challenge command and then find the flag keyword the search for the right argument which will print the flag.

### What I Learned : we can search the manual using / and ? and traverse the results using n and N.


## Searching for Manuals

### Objective : how to find man for the flag command by searching man man.

Flag : `pwn.college{416NiDoXcUpMYovRwXBcquNlfmY.QX2EDO0wCO3EzNzEzW}`

```
man man
apropos challenge
man iocpovwcqu
/challenge/challenge --iocpov 416
```
### Solution : first we search the keyword flag in man by using apropos and then we find the manual where the print flag argument is hidden then we read them manual of the hidden manual and find the argument for the flag

### What I Learned : we can use apropos command to search keyword in man.


## Helpful Programs

### Objective : how to look at documentation of a program without using man but with -help.

Flag : `pwn.college{4C14ufkXdp0qfcjuxZjzm0vBW_7.QX3IDO0wCO3EzNzEzW}`

```
/challenge/challenge --help
/challenge/challenge -p
/challenge/challenge -g 414
```
### Solution : we find the argument that prints us the flag using the --help on the challenge command.

### What I Learned : we can also use --help or -h to look for the documentation of a function.


## Help for Builtins

### Objective : to understand what are builtins and how their documention can be found.

Flag : `pwn.college{ok_Bgv83kVdhhzZOwGCu0b5cKFJ.QX0ETO0wCO3EzNzEzW}`

```
help challenge
challenge --secret ok_Bgv83
```
### Solution : we first use the help command to find the arguments to print the flag for the command builtin and then after finding it we find the flag by passing the secret value in --secret

### What I Learned : what is the difference between the doc reading of builtins and the rest.
