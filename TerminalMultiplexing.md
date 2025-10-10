# Terminal Multiplexing

## Launching Screen

For this challenge, we've hooked things up so that just launching screen will get you the flag.

### Solve
**Flag:** pwn.college{Y1ko-xsQJLZqqKe8KbFcCSVO_sZ.0VN4IDOxwCN3AzNzEzW}
 

```bash
screen
pwn.college{Y1ko-xsQJLZqqKe8KbFcCSVO_sZ.0VN4IDOxwCN3AzNzEzW}
```

### New Learnings
`screen` command to make virtual terminals it starts a screen session.


## Detaching and attaching

For this challenge, you'll need to:

1. Launch screen
2. Detach from it.
3. Run /challenge/run (this will secretly send the flag to your detached session!)
4. Reattach to see your prize

### Solve
**Flag:** pwn.college{sN686JsM843oejN7q87NYp6zBVU.0lN4IDOxwCN3AzNzEzW}

 started the screen session then detached by pressing ctrl-A-D then reattached to the screen as 
 screen -r 139.pts-0.terminal-multiplexing~detaching-and-attaching to get the flag.

```bash
screen
ctrl-a-d
screen -r 139.pts-0.terminal-multiplexing~detaching-and-attaching
Yes! Flag is: pwn.college{sN686JsM843oejN7q87NYp6zBVU.0lN4IDOxwCN3AzNzEzW}
```

### New Learnings
detach from screen ctrl-A-D and retach to the screen screen -r .


## Finding sessions

In this challenge, we've created three screen sessions for you.
One of them contains the flag. The other two are decoys!

### Solve
**Flag:** 
 

```bash

```

### New Learnings
