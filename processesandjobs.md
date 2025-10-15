# Processes and Jobs


## Listing processes

### Objective : To learn how to list processes running in the terminal.

Flag : `pwn.college{sewGsaM9voK7Kv0eNjjU5Dqp1uR.QX4MDO0wCO3EzNzEzW}`

```
ps auxww
/challenge/26050-run-18648
```
### Solution : we first list all the running processes using ps auxww and then see that there is /challenge/26050-run-18648 running and then we run the file to get the flag.

### What I Learned : we can use ps -ef or ps aux to list all the process running in terminal.


## Killing processes

### Objective : To learn how to terminate a process in terminal.

Flag : `pwn.college{MEBy99UoYtbVmU3LD4eraxw0lfj.QXyQDO0wCO3EzNzEzW}`

```
ps -ef | grep dont_run
kill 136
/challenge/run
```
### Solution : we first found the PID of the /challenge/dont_run to then terminate it with the kill command then run the /challenge/run to find the flag.

### What I Learned : we can use the kill command to terminate processes in terminal.


## Interupting processes

### Objective : To learn how to interupt processes in terminal.

Flag : `pwn.college{QpQ8-81M68Cdddji8CwcRVWPwOi.QXzQDO0wCO3EzNzEzW}`

```
/challenge/run
```
### Solution : we first run the /challenge/run and then interupt it with ctrl+c to get the flag.

### What I Learned : we can interupt ongoing process with ctrl+c.


## Killing misbehaving processes

### Objective : To get deep understanding on the above.

Flag : `pwn.college{wY2Tp4dGjSTGcgo7XAAAZ7PuSRw.0FNzMDOxwCO3EzNzEzW}`

```
ps auxww
kill 142
/challenge/run
cat /tmp/flag_fifo
```
### Solution : we first check all the running processes then find the PID for the decoy and the terminate it with the kill command and the run /challenge/run to send the data to the named pipe and then from another terminal i cat the named pipe to find the flag.

### What I Learned : revision and deep understanding of the above topics.


## Suspending processes

### Objective : To learn how to suspend and resume processes in terminal.

Flag : `pwn.college{s-e7Y0VVuxnjNjmjV8STLWj_7RA.QX1QDO0wCO3EzNzEzW}`

```
/challenge/run
(Ctrl-Z)
/challenge/run
```
### Solution : we run the /challenge/run the first time and then suspend it with ctrl-z and then run it back again to get the flag. 

### What I Learned : we can suspend ongoing processes using ctrl-z in terminal.


## Resuming process

### Objective : To learn how to resume suspended processes in terminal.

Flag : `pwn.college{0FedG46opw0Ttctl7P1gApoVpiW.QX2QDO0wCO3EzNzEzW}`

```
/challenge/run
(Ctrl-Z)
fg
```
### Solution : we first run /challenge/run then suspend it with ctrl-z and then resume it with fg command.

### What I Learned : we can resume suspended processes using fg in terminal.


## Backgrounding processes

### Objective : To learn how to make resume suspended processes as background processes.

Flag : `pwn.college{UYw_K6vgXCEGNw3ns5SJv7vREWQ.QX3QDO0wCO3EzNzEzW}`

```
/challenge/run
(Ctrl-Z)
bg
/challenge/run
```
### Solution : we first run /challenge/run then suspend it and then make it a background process using bg and then run it once again to get the flag.

### What I Learned : we use bg to make suspended process to a background process in terminal.


## Foregrounding process

### Objective : To learn how to foreground a background process in terminal.

Flag : `pwn.college{MfrMOyL4wQMIyLVKTvtrU54pri2.QX4QDO0wCO3EzNzEzW}`

```
/challenge/run
(Ctrl-Z)
bg
fg
```
### Solution : we first run the program then suspend it then background the process and then foreground it using fg to get the flag.

### What I Learned : we can foreground background process using fg in terminal.


## Starting backgrounded processes

### Objective : To learn how to background a process without suspending it first.

Flag : `pwn.college{E7lsjkX1y5lX4ZeSOBMbPRHcKj-.QX5QDO0wCO3EzNzEzW}`

```
/challenge/run &
```
### Solution : we can directly put /challenge/run as a background process using &.

### What I Learned : we can append & after a program to directly make it a background process in terminal.


## Process exit codes

### Objective : To learn about exit codes in terminal.

Flag : `pwn.college{QrFfhOu9eqWZKcjSu3xc_ZuJcoz.QX5YDO1wCO3EzNzEzW}`

```
/challenge/get-code
echo $?
/challenge/submit-code 186
```
### Solution : we first run /challenge/get-code for it to end with a exit code then we use echo $? to get the special exit code and then pass it as argument in challenge/submit-code to get the flag.

### What I Learned : we use echo $? to get exit code of latest terminated process.