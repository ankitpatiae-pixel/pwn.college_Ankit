# Pondering PATH

## The PATH variable

In this level, you will disrupt the operation of the /challenge/run program.
This program will DELETE the flag file using the rm command.
 
### Solve
**Flag:**  pwn.college{8oRD465E1eOF4V5l-4FVIBEtUL9.QX2cDM1wCN3AzNzEzW}

```bash
mkdir -p /tmp/empty
export PATH=/tmp/empty
/challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: command not found
The flag is still there! I might as well give it to you!
pwn.college{8oRD465E1eOF4V5l-4FVIBEtUL9.QX2cDM1wCN3AzNzEzW}
```

### New Learnings
PATH command to redirect shell command directories.


## Setting PATH

in this level's /challenge/run will run the win command via its bare name, 
but this command exists in the /challenge/more_commands/ directory, 
which is not initially in the PATH. The win command is the only thing that /challenge/run needs,
so you can just overwrite PATH with that one directory.
 
### Solve
**Flag:**  pwn.college{swLJEg7dimq0DGV3GGwHWgIe6bI.QX1cjM1wCN3AzNzEzW}

```bash
cd /
export PATH=/challenge/more_commands/
/challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{swLJEg7dimq0DGV3GGwHWgIe6bI.QX1cjM1wCN3AzNzEzW}
```

### New Learnings
i can now set PATH to different directories


## Finding Commands

In this challenge, we added a win command somewhere in your $PATH,
but it won't give you the flag. Instead, it's in the same directory as a flag file that we made readable by you! You must find win (with the which command),
and cat the flag out of that directory.
 
### Solve
**Flag:**  pwn.college{EVcVcmLC_nqJVKj4Op87TIWHaeI.01NzEzNxwCN3AzNzEzW}

```bash
which win
/challenge/paths/11673/win
cd /challenge/paths/11673
cat flag
pwn.college{EVcVcmLC_nqJVKj4Op87TIWHaeI.01NzEzNxwCN3AzNzEzW}
```

### New Learnings
i can now find commands using which command.


## Adding Commands

In this challenge we will learn to make a shell script and add its location to the PATH.
 
### Solve
**Flag:**  pwn.college{8Jvt1XGB5ursDR5LDKZuX1XjGy4.QX2cjM1wCN3AzNzEzW}

```bash
mkdir /tmp/mybin
cat > /tmp/mybin/win <<'EOF'
/bin/cat /flag
EOF
chmod +x /tmp/mybin/win
export PATH=/tmp/mybin
/challenge/run
Invoking 'win'....
pwn.college{8Jvt1XGB5ursDR5LDKZuX1XjGy4.QX2cjM1wCN3AzNzEzW}
```

### New Learnings
i can now make shell scripts, add it to PATH to invoke commands.


## Hijacking Commands

In this challenge we will learn to make a shell script and add its location to the PATH.
 
### Solve
**Flag:**  pwn.college{Qj25gRhMbDwR3LnIkeyADmKuHrw.QX3cjM1wCN3AzNzEzW}

```bash
mkdir -p /tmp/mybin
cat > /tmp/mybin/rm <<'SH'
/bin/cat /flag
exit 0
SH
chmod +x /tmp/mybin/rm
export PATH=/tmp/mybin:$PATH
/challenge/run
Trying to remove /flag...
Found 'rm' command at /tmp/mybin/rm. Executing!
pwn.college{Qj25gRhMbDwR3LnIkeyADmKuHrw.QX3cjM1wCN3AzNzEzW}
```

### New Learnings
proficiency in creating commands and setting PATH environment for it.

