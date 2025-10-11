# Perceiving Permissions

## Changing file ownership

In this level, we will practice changing the owner of the /flag file to the hacker user, and then read the flag. For this challenge only, I made it so that you can use chown to your heart's content as the hacker user (again, typically, this requires you to be root). Use this power wisely and chown away!
 
### Solve
**Flag:**  pwn.college{EcfOgDcMOxHZRcY_EPeXK-lAmpj.QXxEjN0wCN3AzNzEzW}

changed directory to / then used chown commad to change owner of the /flag then cat the flag.

```bash
cd /
chown hacker flag
cat flag
pwn.college{EcfOgDcMOxHZRcY_EPeXK-lAmpj.QXxEjN0wCN3AzNzEzW}
```

### New Learnings
changing ownership of files using chown command.


## Groups and files

In this challenge we will how to change group ownership for a file.
 
### Solve
**Flag:**  pwn.college{EcfOgDcMOxHZRcY_EPeXK-lAmpj.QXxEjN0wCN3AzNzEzW}

changed group ownership as chgrp hacker flag then cat the flag.

```bash
id
uid=1000(hacker) gid=1000(hacker) groups=1000(hacker)
cd /
ls -l flag
-r--r----- 1 root root 60 Oct 11 17:21 flag
chgrp hacker flag
cat flag
pwn.college{UDIjEZS2DJjmBiMOU8OVJikzlwG.QXxcjM1wCN3AzNzEzW}
```

### New Learnings
changing group ownership of files using chgrp command.


## Fun With Groups Names

I have randomized the name of the group that your user is in. You will need to use the id command to figure that name out, then chgrp to victory!
 
### Solve
**Flag:**  pwn.college{8lLHMtpCgfIc6-JPmTtNlqxngbB.QXycjM1wCN3AzNzEzW}

changed directory to / then used chown commad to change owner of the /flag then cat the flag.

```bash
cd /
id
uid=1000(hacker) gid=1000(grp15575) groups=1000(grp15575)
chgrp grp15575 flag
cat flag
pwn.college{8lLHMtpCgfIc6-JPmTtNlqxngbB.QXycjM1wCN3AzNzEzW}
```

### New Learnings
using id and chgrp to get the flag.


## Changing permissions

In this challenge, you must change the permissions of the /flag file to read it!
 
### Solve
**Flag:**  pwn.college{ASOtbk7veZ3rNWUgZBs4Zc9WPH0.QXzcjM1wCN3AzNzEzW}

```bash
cd /
chmod a+r /flag
cat flag
pwn.college{ASOtbk7veZ3rNWUgZBs4Zc9WPH0.QXzcjM1wCN3AzNzEzW}
```

### New Learnings
i can now change file permissions.


## Executable Files

In this challenge, the /challenge/run program will give you the flag, but you must first make it executable! Remember your chmod, and get /challenge/run to tell you the flag!
 
### Solve
**Flag:**  pwn.college{UTsFZAgSSx9OWRBWGR-uzBJ3uyI.QXyEjN0wCN3AzNzEzW}

```bash
cd /
chmod a+x /challenge/run
/challenge/run
Successful execution! Here is your flag:
pwn.college{UTsFZAgSSx9OWRBWGR-uzBJ3uyI.QXyEjN0wCN3AzNzEzW}
```

### New Learnings
using chmod to change permissions for programs to make it executable.


## Permission tweaking practice

If you get the permissions right eight times in a row, the challenge will let you chmod /flag to make it readable for yourself :-)
 
### Solve
**Flag:**  pwn.college{ABFmmNRsPp9jkXLprhfzDIGHuzj.QXwEjN0wCN3AzNzEzW}

```bash
chmod u+rwx, g+rx-w, o+rx-w /challenge/pwn
chmod u+rwx,g+rx-w,o+rx-w /challenge/pwn
chmod a+rwx /challenge/pwn
chmod u+x-rw,g+x-rw,o+rwx /challenge/pwn
chmod u-rwx,g+x-rw,o+r-wx /challenge/pwn
chmod u-rwx,g+x-rw,o+rx-w /challenge/pwn
chmod u+w-rx,g+x-rw,o+rwx /challenge/pwn
chmod u+w-rx,g-rwx,o+rwx /challenge/pwn
chmod a+rwx /flag
cat /flag
pwn.college{ABFmmNRsPp9jkXLprhfzDIGHuzj.QXwEjN0wCN3AzNzEzW}
```

### New Learnings
practice of chmod using [+,-] .


## Permission setting practice

This level extends the previous level by requesting more radical permission changes, which you will need = and ,-chaining to achieve. Good luck!
 
### Solve
**Flag:**  pwn.college{wAFODMCuiDcPFKP0LC-1GikNS5K.QXzETO0wCN3AzNzEzW}

problem we'll solve 8 rounds of [chmod].

### New Learnings
practice in chmod using [=] instead of [+,-].


## The SUID Bit

In this challenge, we will execute programs with SUID permission. The "Set User ID" (SUID) permissions bit allows the user to run a program as the owner of that program's file.
 
### Solve
**Flag:**  pwn.college{YdV9jl7b0KxSZ3GocB4-eJxip6Z.QXzEjN0wCN3AzNzEzW}

```bash
chmod a+s /challenge/getroot
/challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root!
Here is your shell...
cat /flag
pwn.college{YdV9jl7b0KxSZ3GocB4-eJxip6Z.QXzEjN0wCN3AzNzEzW}
```

### New Learnings
i can now add +s permissions to files such that the program becomes executable with SUID.
