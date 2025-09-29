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

passed --giveflag argument on /challenge/challenge  

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
Use of argument.


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
Searching in a manual using / command.














