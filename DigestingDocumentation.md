# Digesting Documentation

## Learning from documentation

The program for this challenge is /challenge/challenge, and you'll need to invoke it properly in order for it to give you the flag.
Let's pretend that this is its documentation

### Solve
**Flag:** pwn.college{0EWT7QJ2ux6vO-124_HAZ0KGcZA.QX0ITO0wCN3AzNzEzW}

passed --giveflag argument on /challenge/challenge  

```bash
/challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{0EWT7QJ2ux6vO-124_HAZ0KGcZA.QX0ITO0wCN3AzNzEzW}
```

### New Learnings
program and argument.


## Learning complex usage

/challenge/challenge program allows you to print arbitrary files to the terminal,
when given the --printfile argument. The argument to the --printfile argument is the path of the flag to read. For example,
/challenge/challenge --printfile /challenge/DESCRIPTION.md will print out the description of the level!

### Solve
**Flag:** pwn.college{c9TCvZojqXScxlOu8uWgjSMdnmA.QX1ITO0wCN3AzNzEzW}

passed printfile argument on /challenge/challenge to get value of /flag. 

```bash
/challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{c9TCvZojqXScxlOu8uWgjSMdnmA.QX1ITO0wCN3AzNzEzW}
```

### New Learnings
program and argument with file to read.


## Readding manuals

The challenge in this level has a secret option that, when you use it, will cause the challenge to print the flag. You must learn this option through the man page for challenge!

### Solve
**Flag:** pwn.college{UsFZxg8IbD4itD6JyranuQxCxhi.QX0EDO0wCN3AzNzEzW}

Read the challenge manual using man challenge then /challenge/challenge --sxgbit 846.

```bash
man challenge
/challenge/challenge --sxgbit 846
Correct usage! Your flag: pwn.college{UsFZxg8IbD4itD6JyranuQxCxhi.QX0EDO0wCN3AzNzEzW}
```

### New Learnings
man command to read a manpage.


## Searching manuals

Find the option that will give you the flag by reading the challenge man page.

### Solve
**Flag:** pwn.college{AKLUXmNd7FExnLHYdUZhXb5JCDc.QX1EDO0wCN3AzNzEzW}

Read the challenge manual searched /flag i found --pmy argument which gave the flag.

```bash
man challenge
/challenge/challenge --pmy
Initializing...
Correct usage! Your flag: pwn.college{AKLUXmNd7FExnLHYdUZhXb5JCDc.QX1EDO0wCN3AzNzEzW}
```

### New Learnings
Searching in a manual using / command inside manpage.


## Searching for manuals

Find the hidden manpage and read it to get the flag.

### Solve
**Flag:** pwn.college{s4A4uHgK0YZ1_lXfjfT1DgzMbQa.QX2EDO0wCN3AzNzEzW}

First read the man man manpage in which i found about about apropos then used it to search for challenge manpage using man -k challenge then read the challenge manpage followed instruction , got the flag.

```bash
man man
man -k challenge
suglfjfgzb (1)       - print the flag!
man suglfjfgzb
/challenge/challenge --suglfj 440
Correct usage! Your flag: pwn.college{s4A4uHgK0YZ1_lXfjfT1DgzMbQa.QX2EDO0wCN3AzNzEzW}
```

### New Learnings
man -k apropos search tool ,Search the short manual page descriptions for keywords and display any matches.


## Helpful programs

In this level, you will practice reading a program's documentation with --help. 

### Solve
**Flag:** pwn.college{UMLgyPZfxegoYDT43xmHam26Oui.QX3IDO0wCN3AzNzEzW}

Read challenge program's help documentation used arguments correctly , got the flag.

```bash
/challenge/challenge -h
/challenge/challenge --fortune
The solution to a problem changes the nature of the problem.
                -- Peer
/challenge/challenge -v
I'm exactly the version I need to be!
/challenge/challenge -p
The secret value is: 432
/challenge/challenge -g 432
Correct usage! Your flag: pwn.college{UMLgyPZfxegoYDT43xmHam26Oui.QX3IDO0wCN3AzNzEzW}
```

### New Learnings
read the programs's documentation using -h or --help.


## Help for Builtins

This challenge's challenge command is a shell builtin, rather than a program. Like before, you need to lookup its help to figure out the secret value to pass to it!

### Solve
**Flag:** pwn.college{oepyuInbz_8cPeLQUaYFVkiBQSU.QX0ETO0wCN3AzNzEzW}

Read the challenge manual searched /flag i found --pmy argument which gave the flag.

```bash
help challenge
/challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "oepyuInb".

challenge --fortune
I think I'm schizophrenic.  One half of me's paranoid and the other half's
out to get him.
challenge --version
I'm exactly the version I need to be!
challenge --secret oepyuInb
Correct! Here is your flag!
pwn.college{oepyuInbz_8cPeLQUaYFVkiBQSU.QX0ETO0wCN3AzNzEzW}
```

### New Learnings
Builtin command help. Gives list of shell builtins by running the builtin help.i can get help on a specific command using builtin help.














