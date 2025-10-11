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
**Flag:** pwn.college{csiFtW7hVnaCRDRfFKG4B7grQj9.01N4IDOxwCN3AzNzEzW}
 
reattaching to different screen to get the flag.

```bash
screen -ls
screen -r session_4275b23ee23deee9
pwn.college{csiFtW7hVnaCRDRfFKG4B7grQj9.01N4IDOxwCN3AzNzEzW}
```

### New Learnings
navigating through screens using -r argument after screen command.


## Switching windows

Attach to the session with screen -r, then use one of the key combinations above to switch to Window 1. Go get that flag!

### Solve
**Flag:** pwn.college{YivKFwfmzkabLxgPjUbd8vdEcbL.0FO4IDOxwCN3AzNzEzW}

attached to screen then switched to window 0 by pressing ctrl-A-0.

```bash
screen -r
ctrl-A-0
> Excellent work! You found window 0!
> Here is your flag: pwn.college{YivKFwfmzkabLxgPjUbd8vdEcbL.0FO4IDOxwCN3AzNzEzW}
```

### New Learnings
switching through different windows in screen.


## Detaching and attaching (tmux)

For this challenge:

1. Launch tmux
2. Detach from it.
3. Run /challenge/run (this will send the flag to your detached session!)
4. Reattach to see your prize

### Solve
**Flag:** pwn.college{sz8lEyYCF6sz147eEgoy4RqU_Xj.0VO4IDOxwCN3AzNzEzW}

launched tmux then detached from tmux by pressing ctrl-B then D then run /challenge/run and attached to tmux as tmux a or tmux attach.

```bash
tmux
ctrl-B , D
/challenge/run
tmux a
Congratulations, here is your flag: pwn.college{sz8lEyYCF6sz147eEgoy4RqU_Xj.0VO4IDOxwCN3AzNzEzW}
```

### New Learnings
attaching and detaching from tmux.


## Switching windows (tmux)

We've created a tmux session with two windows:

1. Window 0 has the flag!
2. Window 1 has your warm welcome.
   Go get that flag!

### Solve
**Flag:**  pwn.college{0JNysVv6Vi_GO5FFuhmC1Ko9iB_.0FM5IDOxwCN3AzNzEzW}

attached to tmux then changed window using [ctrl-B,W] then switched to window 0 to get the flag.

```bash
tmux
cltr-B , W

(0)   - challenge_session: 2 windows (attached)

> Excellent work! You found window 0!
> Here is your flag: pwn.college{0JNysVv6Vi_GO5FFuhmC1Ko9iB_.0FM5IDOxwCN3AzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{0JNysVv6Vi_GO5FFuhmC1Ko9iB_.0FM5IDOxwCN3AzNzEzW}
```

### New Learnings
switching through windows in tmux using [ctrl-B,W].
