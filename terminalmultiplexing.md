# Terminal Multiplexing


## Launching screen

### Objective : To learn how to make virtual terminals inside our terminal.

Flag : `pwn.college{0MrOzmhg-GeDYXT4MOLueoad_jn.0VN4IDOxwCO3EzNzEzW}`

```
screen
```
### Solution : we launch a virtual terminal using screen command.

### What I Learned : we can create virtual terminals using screen.


## Detaching and Attaching

### Objective : To learn how to attach and detach virtual terminals.

Flag : `pwn.college{wuL3-JjQAENM4YYfJiM6SFsVNXm.0lN4IDOxwCO3EzNzEzW}`

```
screen
(Ctrl+A then d)
/challenge/run
screen -r
```
### Solution : we first go into a screen and then detach and run the /challenge/run and then reattach using screen -r.

### What I Learned : we can detach using ctrl+a then d and detach using screen -r.


## Finding sessions

### Objective : To learn how to find existing sessions and how to retach to them.

Flag : `pwn.college{0OkM3q_DblzDaJbHz2ZNODKmPXZ.01N4IDOxwCO3EzNzEzW}`

```
screen -ls
screen -r 144
```
### Solution : we first list all the existing screen sessions with screen -ls and then we retach to the sessions one by one to find the flag.

### What I Learned : we can list all the exisisting screen sessions using screen -ls and we can retach to a particular session using screen -r (PID or name).


## Switching windows

### Objective : To learn how to use windows inside a screen session.

Flag : `pwn.college{EGn2Hkm7yE9SG9ii9Vfum61r7DS.0FO4IDOxwCO3EzNzEzW}`

```
screen -r
(Ctrl+A p)
```
### Solution : we first reattach to the screen sessions and then land in windows 1 to go to window 0 we press ctrl+a then p.

### What I Learned : we can go the previous or forward window in a screen session using ctrl+a (p or n).


## Detaching and Attaching (tmux)

### Objective : To learn how to use tmux.

Flag : `Congratulations, here is your flag: pwn.college{4lb5pTUu-hbmBCj_LyUj-crmqQu.0VO4IDOxwCO3EzNzEzW}`

```
tmux
(ctrl+B then d)
/challenge/run
tmux a
```
### Solution : we first launch a tmux sessions then detach from it and then run /challenge/run and then attach to it to obtain the flag.

### What I Learned : we can detach from tmux using ctrl+B then d and attach to tmux using tmux a.


## Switching windows (tmux)

### Objective : To learn how to switch windows in tmux.

Flag : `pwn.college{8ZkmI5N8cRiTuHuaM8kXMAXPmtF.0FM5IDOxwCO3EzNzEzW}`

```
tmux a
(ctrl+B then p)
```
### Solution : we first attach to tmux session and land on window 1 then use ctrl+B then p to go to window 0 to get the flag.

### What I Learned : we can switch window in tmux using ctrl+B (n/p).