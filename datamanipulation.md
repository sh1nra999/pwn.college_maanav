# Data Manipulation


## Translating characters

### Objective : To learn how to translate characters in terminal. 

Flag : `pwn.college{cPeGHBiC2BQmm4BAG0QZnU9H6yq.01MxEzNxwCO3EzNzEzW}`

```
/challenge/run | tr '[:lower:][:upper:]' '[:upper:][:lower:]'
```
### Solution : we first pipe the output of /challenge/run to tr to swap lower case to upper case and upper case to lower case.

### What I Learned : how to use tr to swap characters and [:lower:] represent all lower case characters (a-z) and [:upper:] represent all upper case characters (A-Z).


## Deleting characters

### Objective : To to delete characters from output.

Flag : `pwn.college{MMrxDL2IRvGAgcChwIhcJqzpu9X.0FNxEzNxwCO3EzNzEzW}`

```
/challenge/run | tr -d ^%
```
### Solution : we first pipe the stdout of /challenge/run to use tr command to delete all characters of ^ and %.

### What I Learned : we can delete characters with tr -d.


## Deleting newlines

### Objective : To learn how to delete newlines.

Flag : `pwn.college{MR66yL61buYv5weMhMa3I1XmfZN.0VNxEzNxwCO3EzNzEzW}`

```
/challenge/run | tr -d "\n"
```
### Solution : we delete newlines by using tr -d "\n" to get the flag.

### What I Learned : we can delete newlines by tr -d "\n".


## Extracting the first lines with head

### Objective : To learn how to get only few lines of the output of a program.

Flag : `pwn.college{Q4-YuOPInKRVPqtfffy9xTZHNXL.0lNxEzNxwCO3EzNzEzW}`

```
/challenge/pwn | head -n 7 | /challenge/college
```
### Solution : we first put the stdout of /challenge/pwn to stdin of head command to extract only the first 7 lines of the output and then pipe it to /challenge/college to find the flag.

### What I Learned : we can use head command to extract lines of the output.


## Extracting specific sections of text

### Objective : To learn how to extract some sections of the output of a program.

Flag : `pwn.college{wPxrdUOxRSwmmoA-_rs6cOzO9ip.01NxEzNxwCO3EzNzEzW}`

```
/challenge/run | cut -d " " -f 1 | tr -d "\n"
/challenge/run | cut -d " " -f 2 | tr -d "\n"
```
### Solution : we first pipe the output of /challenge/run to cut command to obtain the characters of the flag from the second column and then pipe it to tr command to remove the lines so that the flag could be obtained in a single line.

### What I Learned : we can use cut -d " " -f to extract columns from an output of a program.


## Sorting data

### Objective : To learn how to sort the given output.

Flag : `pwn.college{4U9QaFtnO-SqygHG5aMDDZmTo58.0FM0MDOxwCO3EzNzEzW}`

```
sort -r /challenge/flags.txt
```
### Solution : we use the sort -r command to reverse sort the text file to obtain the file.

### What I Learned : we can use the sort command to order the output.