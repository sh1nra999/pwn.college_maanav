# Untangling Users


## Becoming root with su

### Objective : To learn how get root with su.

Flag : `pwn.college{0lvdBKCNdsLd3vfauUUBs7sxgA6.QX1UDN1wCO3EzNzEzW}`

```
su
cat /flag
```
### Solution : we first access root permission with su and then provide it with the correct password then become root to access the /flag.

### What I Learned : we can have root access with su in terminal.


## Other users with su

### Objective : To learn how switch to other users using su.

Flag : `pwn.college{gGp8gGIUGvJqijxS_pa9n0Q5PM4.QX2UDN1wCO3EzNzEzW}`

```
su zardus
/challenge/run
```
### Solution : we first switch to zardus usingsu and then run the program to get the flag.

### What I Learned : we can switch users using su in terminal.


## Cracking passwords

### Objective : 

Flag : `pwn.college{8OVBwIs-pvuTdYtUWR3xkQTEQNm.QX3UDN1wCO3EzNzEzW}`

```
john /challenge/shadow-leak
john --show /challenge/shadow-leak
su zardus
/challenge/run
```
### Solution : we first crack the password using john and then use the cracked password to login as zardus and then run /challenge/run to get the flag.

### What I Learned : we can use john to crack encrypted password.


## Using sudo

### Objective : To learn the difference between su and sudo.

Flag : `pwn.college{Y3K-qqPBGqaR9B1KT4woCVWsd6i.QX4UDN1wCO3EzNzEzW}`

```
sudo cat /flag
```
### Solution : we use the sudo command to cat the /flag file to find the flag.

### What I Learned : we now use sudo instead of su as sudo checks the permission neccessary to run the command instead of launching full fledged root shell.