# Processes and Jobs

## Listing Processes

In this level, I have once again renamed /challenge/run to a random filename, and this time made it so that you cannot ls the /challenge directory! But I also launched it, so you can find it in the running process list, figure out the filename, and relaunch it directly for the flag! 

### Solve
**Flag:** pwn.college{YDNw9whO6eHqKc1FO0iMN4kHJbN.QX4MDO0wCN3AzNzEzW}

got all the files running using ps command with argument -ef as ps -ef then read the running /challenge/run file which was renamed as /challenge/9689-run-1632.

```bash
ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 07:26 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/
root           7       1  0 07:26 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 07:26 ?        00:00:00 /challenge/9689-run-1632
root         135     132  0 07:26 ?        00:00:00 sleep 6h
hacker       137       0  0 07:26 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qz
hacker       143     137  0 07:26 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       154     143  0 07:26 pts/0    00:00:00 ps -ef
/challenge/9689-run-1632
Yahaha, you found me! Here is your flag:
pwn.college{YDNw9whO6eHqKc1FO0iMN4kHJbN.QX4MDO0wCN3AzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').

```

### New Learnings
ps command and arguments -ef and aux.


## Killing Processes

In this challenge, /challenge/run will refuse to run while /challenge/dont_run is running! You must find the dont_run process and kill it. If you fail, pwn.college will disavow all knowledge of your mission. 

### Solve
**Flag:**  pwn.college{gKglgwM6Ym5UIeLjXWgr-MnJgvn.QXyQDO0wCN3AzNzEzW}

used ps command with argument aux to see the PID of /challenge/dont_run then used kill command to close the process as kill /challenge/dont_run. 

```bash
ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   07:35   0:00 /sbin/docker-init -
root           7  0.0  0.0 231708  2560 ?        S    07:35   0:00 /run/dojo/bin/sleep
root         135  0.0  0.0   5204  3520 ?        S    07:35   0:00 su -c /challenge/.l
hacker       136  0.0  0.0 231576  3520 ?        Ss   07:35   0:00 /challenge/dont_run
hacker       137  0.0  0.0 231708  2560 ?        S    07:35   0:00 sleep 6h
hacker       139  0.0  0.0 231576  3520 pts/0    Ss   07:35   0:00 /nix/store/0nxvi9r5
hacker       145  0.0  0.0 231940  4160 pts/0    S+   07:35   0:00 /run/dojo/bin/bash
hacker       167  0.0  0.0 231576  3520 pts/1    Ss   07:37   0:00 /nix/store/0nxvi9r5
hacker       173  0.0  0.0 231940  4160 pts/1    S    07:37   0:00 /run/dojo/bin/bash
hacker       190  0.0  0.0 233600  3840 pts/1    R+   07:39   0:00 ps aux
kill 136
/challenge/run
Great job! Here is your payment:
pwn.college{gKglgwM6Ym5UIeLjXWgr-MnJgvn.QXyQDO0wCN3AzNzEzW}
```

### New Learnings
kill command can close a running process.


## Interrupting Processes

In this challenge, /challenge/run will refuse to give you the flag until you interrupt it.  

### Solve
**Flag:**  pwn.college{cSeeIRpoUtvbIxd8MoZwK_dk2Is.QXzQDO0wCN3AzNzEzW}

run /challenge/run then pressed c while holding ctrl.

```bash
/challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{cSeeIRpoUtvbIxd8MoZwK_dk2Is.QXzQDO0wCN3AzNzEzW}
```

### New Learnings
ctrl-C interrupts the process running.it causes the application to cleanly exit.


## Killing misbehaving processes

In this challenge, there's a decoy process that's hogging a critical resource - a named pipe (FIFO) at /tmp/flag_fifo into which (like in the Practicing Piping FIFO challenge) /challenge/run wants to write your flag. You need to kill this process.

Your general workflow should be:

1. Check what processes are running.
2. Find /challenge/decoy in the list and figure out its process ID.
3. kill it.
4. Run /challenge/run to get the flag without being overwhelmed by decoys (you don't need to
   redirect its output; it'll write to the FIFO on its own).


### Solve
**Flag:**  


```bash

```

### New Learnings

