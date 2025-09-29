# File Globbing

## Matching with *

 Starting from your home directory, change your directory to /challenge, 
 but use globbing to keep the argument you pass to cd to at most four characters! 
 Once you're there, run /challenge/run for the flag!

### Solve
**Flag:** pwn.college{MyT_YRgPArRq_JWNO3p0XZaGjwO.QXxIDO0wCN3AzNzEzW}

changed directory to /challenge using * Glob as cd /*ge.

```bash
cd /*ge
/challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{MyT_YRgPArRq_JWNO3p0XZaGjwO.QXxIDO0wCN3AzNzEzW}
```

### New Learnings
Glob * it replaces the argument that matches any pattern.


## Matching with ?

Starting from your home directory, change your directory to /challenge,
but use the ? character instead of c and l in the argument to cd! Once you're there, 
run /challenge/run for the flag!

### Solve
**Flag:** pwn.college{oaLgUD1h5SNmPhP4E_5ivvyFVNr.QXyIDO0wCN3AzNzEzW}

changed directory to /challenge using ? Glob as cd /?ha??enge.

```bash
cd /?ha??enge
/challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{oaLgUD1h5SNmPhP4E_5ivvyFVNr.QXyIDO0wCN3AzNzEzW}
```

### New Learnings
Glob ? it replaces single character of an argument.


## Matching with []

Change your working directory to /challenge/files and run /challenge/run 
with a single argument that bracket-globs into file_b, file_a, file_s, and file_h!

### Solve
**Flag:** pwn.college{UjfZUGH5gm1uihPkmUF64I5qviG.QXzIDO0wCN3AzNzEzW}

changed directory to /challenge/files run /challenge/run with [] glob as /challeng/run file_[bash].

```bash
cd /challenge/files
/challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{UjfZUGH5gm1uihPkmUF64I5qviG.QXzIDO0wCN3AzNzEzW}
```

### New Learnings
Glob [] it is a limited form of ? glob it access the single characters of files specified inside [].


## Matching paths with []

Starting from your home directory, run /challenge/run with a single argument that 
bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files!

### Solve
**Flag:** pwn.college{UjfZUGH5gm1uihPkmUF64I5qviG.QXzIDO0wCN3AzNzEzW}

run the /challenge/run with absolute path of files as /challenge/files/file[bash].

```bash
/challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{IHosDRtA7ez_7ovn0jnVKVxQXPO.QX0IDO0wCN3AzNzEzW}
```

### New Learnings
using [] glob with absolute path of the files.


## Multiple Globs

cd to /challenge/files and run /challenge/run, providing a single argument: a short (3 characters or less) 
globbed word with two * globs in it that covers every word that contains the letter p.

### Solve
**Flag:** pwn.college{sSuCtwRRbECqcGAU5P-lXmkKfjt.0lM3kjNxwCN3AzNzEzW}

Change directory to /challenge/files then run the /challenge/run with two * globs and single argument p as /challenge/run *p*.

```bash
cd /challenge/files
/challenge/run *p*
You got it! Here is your flag!
pwn.college{sSuCtwRRbECqcGAU5P-lXmkKfjt.0lM3kjNxwCN3AzNzEzW}
```

### New Learnings
multiple globs for a single argument.


## Mixing Globs

cd to /challenge/files and using the globbing you've learned, write a single,
short (6 characters or less) glob that (when passed as an argument to /challenge/run) 
will match the files "challenging", "educational", and "pwning"!

### Solve
**Flag:** pwn.college{YY5YvmdcbEWMO7W-VO4E1mQL5PI.QX1IDO0wCN3AzNzEzW}

run the /challenge/run with [cep]* argument as c,e,p are the first letter of the file names thats why its inside the [] glob.

```bash
/challenge/run [cep]*
You got it! Here is your flag!
pwn.college{YY5YvmdcbEWMO7W-VO4E1mQL5PI.QX1IDO0wCN3AzNzEzW}
```

### New Learnings
mixed globs for argument.


## Exclusionary Globbing

cd to /challenge/files and run /challenge/run with all files that don't start with
p, w, or n!

### Solve
**Flag:** pwn.college{EGm2fWIwFl9bPsN0-lelZqQaag3.QX2IDO0wCN3AzNzEzW}

cd to /challenge/files the use ! to run /challenge/run with all the files not starting from p,w,n as /challenge/run [pwn]* .

```bash
cd /challenge/files
/challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{EGm2fWIwFl9bPsN0-lelZqQaag3.QX2IDO0wCN3AzNzEzW}
```

### New Learnings
! or ^ inverts the funtion of the glob used with.


## Tab completeion

This challenge has copied the flag into /challenge/pwncollege, and you can freely cat that file.
But you can't type the filename: we used some serious trickery to make sure that you must tab-complete it. 
Try it out!

### Solve
**Flag:** pwn.college{8aFmlZ3s9Fz7ovXZlWfsvKfEx0Z.0FN0EzNxwCN3AzNzEzW}

pressed tab after cha<TAB> and after pwnco<TAB> as cat /cha<TAB>/pwnco<TAB>.

```bash
cat /cha<TAB>/pwnco<TAB>
pwn.college{8aFmlZ3s9Fz7ovXZlWfsvKfEx0Z.0FN0EzNxwCN3AzNzEzW}
```

### New Learnings
Tab key can expand the name which i am writting.


## Multiple options for Tab completeion

This challenge has a /challenge/files directory with a bunch of files starting with pwncollege.
Tab-complete from /challenge/files/p or so, and make your way to the flag!

### Solve
**Flag:** pwn.college{wIt0JBcpR7S_cIG9jrVbQrIDyYy.0lN0EzNxwCN3AzNzEzW}

pressed f1 key the 2 times tab key which printed all the files under that directory then used cat to get the flag.

```bash
/challenge/files/pwn<f1><TAB><TAB>
pwn                    pwncollege-family      pwncollege-flyswatter
pwn-college            pwncollege-flag        pwncollege-hacking
pwn-the-planet         pwncollege-flamingo
cat /challenge/files/pwncollege-flag
pwn.college{wIt0JBcpR7S_cIG9jrVbQrIDyYy.0lN0EzNxwCN3AzNzEzW}
```

### New Learnings
using f1 key and then pressing tab key 2nd time prints all the files under that particular directory.


## Tab completeion on commands

This level has a command that starts with pwncollege, and it'll give you the flag. 
Type pwncollege and hit the tab key to auto-complete it!

### Solve
**Flag:** pwn.college{4kLfUgGQrG1TpVvNNlnEmR8z9r7.0VN0EzNxwCN3AzNzEzW}

pressed tab to complete pwncollege command as pwncol<TAB>' then it expands the command as pwncollege-21423 entered that and got the flag.

```bash

pwncol<TAB>
pwncollege-21423
Correct! Here is your flag:
pwn.college{4kLfUgGQrG1TpVvNNlnEmR8z9r7.0VN0EzNxwCN3AzNzEzW}
```

### New Learnings
Tab can be used with commands.





