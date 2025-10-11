# Chaining commands

## Chaining with semicolons

Give it a try now! In this level,
you must run /challenge/pwn and then /challenge/college, chaining them with a semicolon.

### Solve
**Flag:**  pwn.college{MlqMXYqM5xUn5hsHRd044yJqH2k.QX1UDO0wCN3AzNzEzW}

chaining /challenge/pwn and /challenge/college with semi-colon as /challenge/pwn ; /challenge/college

```bash
/challenge/pwn ; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{MlqMXYqM5xUn5hsHRd044yJqH2k.QX1UDO0wCN3AzNzEzW}
```

### New Learnings
chaining two commands into a single line using semi-colon.


## Building on Success

In this challenge, you need to chain the programs /challenge/first-success and 
/challenge/second using the && operator.

### Solve
**Flag:** pwn.college{URZ8T-_yc7y_yGad3dp69cB8fOs.0lM0MDOxwCN3AzNzEzW}

chaining /challenge/first-success and /challenge/second using && as /challenge/first-success && /challenge/second


```bash
/challenge/first-success
/challenge/second

Error: /challenge/first-success must be successfully chained with
/challenge/second using &&

/challenge/first-success && /challenge/second

Nice chaining! Flag: pwn.college{URZ8T-_yc7y_yGad3dp69cB8fOs.0lM0MDOxwCN3AzNzEzW}
```

### New Learnings
chaining programs using && operator . second program will only run when the first program executes successfully. 


## Handling failure

In this challenge, you need to chain /challenge/first-failure and /challenge/second using the || operator. Go for it!

### Solve
**Flag:**  pwn.college{QTNDr9SWmfsI3O9YCIMrEZ54EXI.01M0MDOxwCN3AzNzEzW}

chained the /challenge/first-failure with /challenge/second as 
/challenge/first-failure || /challenge/second


```bash
/challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{QTNDr9SWmfsI3O9YCIMrEZ54EXI.01M0MDOxwCN3AzNzEzW}
```

### New Learnings
chaining two programs with || operator works only if the first command fails.


## Your first shell script

Same as last level, run /challenge/pwn and then /challenge/college,
but this time in a shell script called x.sh, then run it with bash!

### Solve
**Flag:**  pwn.college{46nny-kt9nqYeEwPHqOs0wfYFSC.QXxcDO0wCN3AzNzEzW}

chained /challenge/pwn and /challenge/college and transfered it to shell x.sh as
echo "/challenge/pwn; /challenge/college" > x.sh

```bash
echo "/challenge/pwn; /challenge/college" > x.sh
bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{46nny-kt9nqYeEwPHqOs0wfYFSC.QXxcDO0wCN3AzNzEzW}
```

### New Learnings
shell script .  shell scrips are named with sh suffix.


## Redirecting script output 

In this level, we will practice piping (|) from your script to another program. Like before, you need to create a script that calls the /challenge/pwn command followed by the /challenge/college command, and pipe the output of the script into a single invocation of the /challenge/solve command!

### Solve
**Flag:**  pwn.college{g14uAVGJZ2nXUV_7eoQoYTSILLH.QX4ETO0wCN3AzNzEzW}

chained /challenge/pwn and /challenge/college and transfered it to shell x.sh as
echo "/challenge/pwn; /challenge/college" > x.sh

```bash
echo "/challenge/pwn; /challenge/college" > x.sh
bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{g14uAVGJZ2nXUV_7eoQoYTSILLH.QX4ETO0wCN3AzNzEzW}
```

### New Learnings
I can now use piping to redirect outputs of a script to another command.


## Executable shell scripts

Try that here! Make a shellscript that will invoke /challenge/solve, make it executable, and run it without explicitly invoking bash!

### Solve
**Flag:**  pwn.college{46nny-kt9nqYeEwPHqOs0wfYFSC.QXxcDO0wCN3AzNzEzW}



```bash
echo "/challenge/solve" > flag.sh
chmod +x /home/hacker/solve.sh
./flag.sh
Congratulations on your shell script execution! Your flag:
pwn.college{gqxDNXn9gMEz6KicgEQeZp7GnbM.QX0cjM1wCN3AzNzEzW}
```

### New Learnings
I can now run shell scripts as executables without the need of bash.


## Understanding Shebangs

For this challenge, create a script at /home/hacker/solve.sh that has a proper shebang and outputs "hack the planet". Remember to make it executable, then run /challenge/run to verify your script works correctly!

### Solve
**Flag:**  pwn.college{sWpb5HggKQ4wY7EknFux51KnEOc.0VOzMDOxwCN3AzNzEzW}

```bash
cat > /home/hacker/solve.sh <<'EOF'
> #!/bin/bash
> echo "hack the planet"
> EOF
chmod +x /home/hacker/solve.sh
/challenge/run
Testing your script...
Perfect! Your flag:
pwn.college{sWpb5HggKQ4wY7EknFux51KnEOc.0VOzMDOxwCN3AzNzEzW}
```

### New Learnings
