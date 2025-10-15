# Practicing Piping


## Redirecting output

### Objective : To learn how to redirect output to another file.

Flag : `pwn.college{MKyOF5cFhdpQ8dme-Pt6l2RFMeV.QX0YTN0wCO3EzNzEzW}`

```
echo PWN > COLLEGE
```
### Solution : i used the > operator to put PWN in COLLEGE. 

### What I Learned : > is used to redirect output to another file.


## Redirecting more output

### Objective : To learn how to redirect the output of any command.

Flag : `pwn.college{41BDaQQwTtX5TYArSGMdUt5bxYR.QX1YTN0wCO3EzNzEzW}`

```
/challenge/run > myflag
cat myflag
```
### Solution : i first redirected the output of /challenge/run to myflag and then print the content of myflag to get the flag.

### What I Learned : we can redirect any command and not just echo with >.


## Appending output

### Objective : To learn how to append redirected output to a file.

Flag : `pwn.college{0YrPxi_RdY9zlHdRDN2FIsTK0Bl.QX3ATO0wCO3EzNzEzW}`

```
/challenge/run >> /home/hacker/the-flag
cat /home/hacker/the-flag
```
### Solution : i first appended the output of /challenge/run to /home/hacker/the-flag and then cat the file to find the flag.

### What I Learned : how to append output to already created file instead of making new output files everytime using >>.


## Redirecting errors

### Objective : To learn how to redirect error of a program to other file.

Flag : `pwn.college{oFnJxAv8xowTJtr9GAVkS4RSYCy.QX3YTN0wCO3EzNzEzW}`

```
/challenge/run > myflag 2> instructions
cat instructions
cat myflag
```
### Solution : i redirected the stdout to myflag and error to instructions and then cat the myflag to find the flag.

### What I Learned : i can redirect errors using 2> and i can redirect the stdout and error of a program in a single line.


## Redirecting input

### Objective : To learn how to redirect input of a command.

Flag : `pwn.college{8WhdqIVoEMQngaGCWfOqi_hZzBl.QXwcTN0wCO3EzNzEzW}`

```
echo COLLEGE > PWN
/challenge/run < PWN
```
### Solution : first i redirected the output of echo COLLEGE to PWN, then redirected the input of /challenge/run to PWN.

### What I Learned : how to redirect input using <.


## Grepping stored results

### Objective : how to filter through the redirected output with grep.

Flag : `pwn.college{kZkxqGliW8iXdT8dUU8JgTjSgcg.QX4EDO0wCO3EzNzEzW}`

```
/challenge/run > /tmp/data.txt
grep 'flag' /tmp/data.txt
grep 'pwn' /tmp/data.txt
```
### Solution : i first redirected the output to /tmp/data.txt then used the grep command to filter through the words to find the flag.

### What I Learned : i revised how to redirect output and how to use grep.


## Grepping live output

### Objective : To learn how to directly put the stdout of a command to stdin of another.

Flag : `pwn.college{4dF5WIXh5xO8N90T4exb_4haDpS.QX5EDO0wCO3EzNzEzW}`

```
/challenge/run | grep 'pwn'
```
### Solution : we first run the /challenge/run and then redirect the stdout of the file to the stdin of grep command to find the flag.

### What I Learned : how the | can be used to redirect stdout to stdin of antoher command.


## Grepping errors

### Objective : To leran how the >& works.

Flag : `pwn.college{kxMw2Bd9x24fwo5RBAXMFhGCjMA.QX1ATO0wCO3EzNzEzW}`

```
/challenge/run 2>& 1 | grep pwn
```
### Solution : i first changed the the redirect of error to stdout to pipe to the grep command to find the flag.

### What I Learned : how to convert error to stdout and use the pipe to use the grep command.


## Filtering with grep -v

### Objective : To learn how to use the grep -v.

Flag : `pwn.college{cVwB6zmrg8cx4rwDB3m7n0pegBr.0FOxEzNxwCO3EzNzEzW}`

```
/challenge/run | grep -v 'DECOY'
```
### Solution : we first pipe the stdout of /challenge/run to grep -v to inverse search the word DECOY to show only lines that do not contain DECOY to find the real flag.

### What I Learned : that we use grep -v to inverse search in a file.


## Duplicating pipe data with tee

### Objective : To learn how to copy data flowing between the pipes.

Flag : `pwn.college{YFAWzhYllefMq7CY7A73HdPcMQK.QXxITO0wCO3EzNzEzW}`

```
/challenge/pwn | tee new.txt
cat new.txt
/challenge/pwn --secret YFAWzhYl | tee new1.txt | /challenge/college
```
### Solution : i first used the tee command to find the output flowing from /challenge/pwn from that i learned the secret argument needed to pass to /challenge/college to find the flag.

### What I Learned : tee can be used between piping to help understand the flow of output data which can help in debugging.


## Proccess substitution for input

### Objective : To learn how to compare the output of two commands using process substitution.

Flag : `pwn.college{YvNOFrZzpHEkgdUoDFjKJFNXyyw.0lNwMDOxwCO3EzNzEzW}`

```
diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
```
### Solution : i used the diff command to find the difference in temp files generated which contain the output of the two commands.

### What I Learned : how to use <() to generate temporary files for commands.


## Writing to multiple programs

### Objective : To learn how to use >().

Flag : `pwn.college{oA_fEvi1Fd9mdsx9zi52uVg4WO8.QXwgDN1wCO3EzNzEzW}`

```
/challenge/hack | tee >(/challenge/planet) | /challenge/the
```
### Solution : we flow the output of /challenge/hack to /challenge/the but in between make a copy of it with tee >(/challenge/planet).

### What I Learned : how >() can be used as stdin for any command.


## Split-piping stderr and stdout

### Objective : To have a deep understanding on piping.

Flag : `pwn.college{IDSjjMagfL1lXb15Nm2SWz66yrc.QXxQDM2wCO3EzNzEzW}`

```
 /challenge/hack 2> >(/challenge/the) | /challenge/planet
```
### Solution : i used 2> to redirect the error to the input of /challenge/the and | to redirect the output to /challenge/planet.

### What I Learned : have a deep understanding on the entire concept.


## Named pipes

### Objective : 

Flag : ``

```

```
### Solution : 

### What I Learned : 