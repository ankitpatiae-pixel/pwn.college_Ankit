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








