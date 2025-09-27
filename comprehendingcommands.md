# Comprehending Commands

## cat: not the pet, but the command!

### Objective : To use cat commandd.

Flag : `pwn.college{IyKEUxlTAuEEqX8oWmQoCQeOEKY.QXxcTN0wCO3EzNzEzW}`

```
cat flag
```
### Solution : use the cat command to print the flag in terminal.

### What I Learned : cat can be used to easily print files in terminal.


## catting absolute paths

### Objective : To use cat with absolute paths.

Flag : `pwn.college{cJnEy0Ky3wNDgFxlKuqtQjcdWrm.QX5ETO0wCO3EzNzEzW}`

```
cat /flag
```
### Solution : we use the cat command with absolute path argument to print the file.

### What I Learned : we can use cat with absolute paths.


## more catting practice

### Objective : To get used and practice cat command.

Flag : `pwn.college{sLluXUtzrjRt4Tu68b2b5xbPqs-.QXwITO0wCO3EzNzEzW}`

```
cat /usr/share/apport/flag
```
### Solution : we use the cat command with absolute path argument to print the file.


## grepping for a needle in haystack

### Objective : To learn the command grep.

Flag : `pwn.college{ool2rVmhR2wd9Tb9223gHaqyaV_.QX3EDO0wCO3EzNzEzW}`

```
grep pwn.college /challenge/data.txt
```
### Solution : we use the grep command with the "pwn.college" string because the flag always starts with this along witht the absolute path of the file.

### What I Learned : grep can be used to find desired line in a file using line pattern as input.


## comparing files

### Objective : To use the diff function to find the flag.

Flag : `pwn.college{oWhtt-BAyRmxx-2JuWDZs4_KoDC.01MwMDOxwCO3EzNzEzW}`

```
diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
```
### Solution : we use the diff command to look for difference between the two files to find the flag.

### What I Learned : diff command can be used to compare two files.


## listing files

### Objective : To list all the files in a directory.

Flag : `pwn.college{sPFCoTVHltVpGa9sruXAhzDlMsZ.QX4IDO0wCO3EzNzEzW}`

```
ls /challenge
/challenge/13868-renamed-run-10062
```
### Solution : we first cd into challenge directory and then list all the files to find the file with the flag.

### What I Learned : ls is used to list all the files in a directory.


## touching files

### Objective : To create new blank files using touch command.

Flag : `pwn.college{Ao3gusmbUyLHy58x3Y5jU7yQO47.QXwMDO0wCO3EzNzEzW}`

```
touch /tmp/pwn
touch /tmp/college
/challenge/run
```
### Solution : we first create two files in /tmp using touch command and then run the file with the flag.

### What I Learned : we can create new empty files using touch command.


## removing files

### Objective : To learn how to delete files.

Flag : `pwn.college{8OagSk7PBCrhhsQwCgGkQ1OJZoe.QX2kDM1wCO3EzNzEzW}`

```
rm delete_me
/challenge/check
```
### Solution : we first delete the file using the rm command and then run the /challenge/check file to get the flag.

### What I Learned : rm is used to dete files in terminal.


## Moving files

### Objective : To learn how to move files in terminal.

Flag : `pwn.college{UX14JkwLoDIzz_1A_WxLdqRQlW8.0VOxEzNxwCO3EzNzEzW}`

```
mv /flag /tmp/hack-the-planet
/challenge/check
```
### Solution : we copy the file /flag to /tmp/hack-the-planet and then run /challenge/check to get the flag.

### What I Learned : mv is used to move files around in terminal.


## hidden files

### Objective : To learn how to view hidden files in terminal.

Flag : `pwn.college{ogg0r7GAorj1lmbYcfF5mt4YOEL.QXwUDO0wCO3EzNzEzW}`

```
cd /
ls -a
cat .flag-233052537823735
```
### Solution : we fist cd into / directory and then list all the files using ls -a and then print the .flag file to find the flag.

### What I Learned : la -a is used to list all the files including hidden ones in the terminal.


## An epic filesystem quest

### Objective : To get familiar with ls, cd and cat command.

Flag : `pwn.college{EoerIwTISieqUEyeM52NUK6L__r.QX5IDO0wCO3EzNzEzW}`

```
cd /
ls -a
file TRACE
cat TRACE
ls -a /usr/local/lib/python3.8/dist-packages/nbformat/__pycache__
cat /usr/local/lib/python3.8/dist-packages/nbformat/__pycache__/GIST-TRAPPED
cd /usr/local/lib/python3.8/dist-packages/setuptools/_vendor/importlib_resources/tests/data01/subdirectory
ls -a
cat EVIDENCE 
ls -a /opt/linux/linux-5.4/sound/soc/amd/include
cat /opt/linux/linux-5.4/sound/soc/amd/include/.CLUE 
ls -a /opt/linux/linux-5.4/drivers/media/platform/sti/bdisp
cat /opt/linux/linux-5.4/drivers/media/platform/sti/bdisp/INSIGHT 
ls -a /usr/share/doc/cpp-aarch64-linux-gnu
cat /usr/share/doc/cpp-aarch64-linux-gnu/.REVELATION
ls -a /usr/lib/terminfo/d
cat /usr/lib/terminfo/d/BLUEPRINT
ls -a /opt/linux/linux-5.4/include/config/cc/has/asm
cat /opt/linux/linux-5.4/include/config/cc/has/asm/.NUGGET
ls -a /var/cache/apache2/mod_cache_disk
cat /var/cache/apache2/mod_cache_disk/SPOILER-TRAPPED
```
### Solution : we just cd-ed and ls-ed into directories to find the files and find the next clue and so on.

### What I Learned : more grasp and practice on the ls, cd and cat command.


## Making directories

### Objective : To learn how to make new directories in terminal.

Flag : `pwn.college{oNl5CU4jlvEpu406PHUFOEXtrAZ.QXxMDO0wCO3EzNzEzW}`

```
mkdir /tmp/pwn
touch /tmp/pwn/college
/challenge/run
```
### Solution : we first make a new directory in /tmp and then make a new file inside the new directory and then get the flag.

### What I Learned : we can make new directories using mkdir command.


## Finding lines

### Objective : To search for a particular file.

Flag : `pwn.college{0F5fDxX9IwtTZhoFMILKfdeEMfe.QXyMDO0wCO3EzNzEzW}`

```
find / -name flag
find / -name flag -type f
cat /opt/linux/linux-5.4/tools/perf/pmu-events/arch/s390/flag
```
### Solution : we use the find command to search the entire database '/' with the keyword flag and '-type f' which only list the files and not the directories.

### What I Learned : we can use find commnad to search for any file in terminal.


## Linking files

### Objective : To soft link two files.

Flag : ``

```

```
### Solution : .

### What I Learned : we learned about how to soft link two file using 'ln -s' and we can get information about any file using 'file' command.
