# Perceiving Permissions


## Changing file ownership

### Objective : To learn how to change ownership of a file in terminal.

Flag : `pwn.college{M8ncg4huwBDV2gASRsfVC-xaXyV.QXxEjN0wCO3EzNzEzW}`

```
chown hacker /flag
cat /flag
```
### Solution : first we change the ownership of the file so that hacker user can access it and then print the flag.

### What I Learned : we change the ownership of a file using chown command.


## Groups and files

### Objective : To learn how to change the group ownership of a file.

Flag : `pwn.college{QSl3rVQ068VGdNadr6S1HE8Nian.QXxcjM1wCO3EzNzEzW}`

```
chgrp hacker /flag
cat /flag
```
### Solution : first i changed the group ownership of the file from root to hacker and then cat it to get the flag.

### What I Learned : we change the group ownership of a file wit chgrp.


## Fun with group names

### Objective : 

Flag : pwn.college{Y0pcP0H70hcKGMm1JSOduJ16Jog.QXycjM1wCO3EzNzEzW}`

```
id
chgrp grp29384 /flag
cat /flag
```
### Solution : we first find the group id of our user using id and then change the group ownership using chgrp to access the flag file.

### What I Learned : revision on id and chgrp commands.


## Changing permissions

### Objective : To learn how to tweak permissions of a file.

Flag : `pwn.college{0h2dA8g4C_JU1VwDsIyfw-6Actt.QXzcjM1wCO3EzNzEzW}`

```
ls -l /flag
chmod ugo+rwx
cat /flag
```
### Solution : we first change the permission of the /flag file so that everyone can access it so we can get the flag.

### What I Learned : we can use chmod to change the permissions of a file in terminal.


## Executable files

### Objective : To learn how to change file permission to make it executable.

Flag : `pwn.college{AvRS1eNgvfHKmGe_PSnSZMQkqcW.QXyEjN0wCO3EzNzEzW}`

```
chmod u+x /challenge/run
/challenge/run
```
### Solution : we first change the file permission so that the user has permission to execute it.

### What I Learned : revision of chmod command.


## Permission tweaking practice

### Objective : To practice chmod.

Flag : `pwn.college{0TLrNLy2VCQiwR8QcYv8sF3Rr9x.QXwEjN0wCO3EzNzEzW}`

```
/challenge/run
chmod ug+x /challenge/pwn
chmod o+x /challenge/pwn
chmod ug-x /challenge/pwn
chmod g-r /challenge/pwn
chmod o-r /challenge/pwn
chmod u-rw /challenge/pwn
chmod ug+rwx /challenge/pwn
chmod ug-wx /challenge/pwn
id
chmod u+rwx /flag
cat /flag
```
### Solution : we alter the permission of the file as said in the challenges and at the end change the permission of the /flag so that the user can access the file.

### What I Learned : revision on chmod.


## Permission setting practice

### Objective : To learn how to set permission with chmod in terminal.

Flag : `pwn.college{w_EnEubRHVD1o_UYUea4av9HYA5.QXzETO0wCO3EzNzEzW}`

```
/challenge/run
chmod u=rwx,g=rx,o=rw /challenge/pwn
chmod u=x,g=rwx,o=rw /challenge/pwn
chmod u=rwx,g=wx,o=rw /challenge/pwn
chmod u=r,g=x,o=- /challenge/pwn
chmod u=w,g=rwx,o=rwx /challenge/pwn
chmod u=rwx,g=rwx,o=rwx /challenge/pwn
chmod u=wx,g=rw,o=r /challenge/pwn
chmod u=x,g=rw,o=wx /challenge/pwn
id
chmod u+rwx /flag
cat /flag
```
### Solution : we set the file permissions according the given conditions to get the flag at the end.

### What I Learned : we can use = after chmod to set the file permissions.


## The SUID bit

### Objective : To learn about the SUID bit in file permissions.

Flag : `pwn.college{4cKDRS2ZZj-s76nRfm8iB_O59VF.QXzEjN0wCO3EzNzEzW}`

```
chmod u+s /challenge/getroot
/challenge/getroot
cat /flag
```
### Solution : we first set the SUID bit to the /challenge/getroot file and then run the file to access root terminal and then cat the flag.

### What I Learned : we can use chmod u+s to give the file SUID bit and what SUID bit does, it gives anyone with executable permisission to execute the file as the owner of the file.