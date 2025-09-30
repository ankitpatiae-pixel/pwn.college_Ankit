# Practicing Piping

## Redirecting output

In this challenge, you must use this output redirection to write the word PWN (all uppercase)
to the filename COLLEGE (all uppercase).

### Solve
**Flag:** pwn.college{IJQnpnRwrfq4K4_07W4w80Qp8qf.QX4cTO0wCN3AzNzEzW}

written echo PWN > COLLEGE this redirected PWN to file COLLEGE. 

```bash
echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{IhM3UBMZdvEsVBATllB8s0uLguA.QX0YTN0wCN3AzNzEzW}
```

### New Learnings
'>' character can redirect output to the file which can be called later and get the output through the file. 


## Redirecting more output

In this challenge, you must use this output redirection to write the word PWN (all uppercase)
to the filename COLLEGE (all uppercase).

### Solve
**Flag:** pwn.college{IJQnpnRwrfq4K4_07W4w80Qp8qf.QX4cTO0wCN3AzNzEzW}

redirected the flag from /challenge/run to myflag file as /challenge/run > myflag.

```bash
/challenge/run > myflag

[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag
.
.
.
.
.
[FLAG] Here is your flag:
[FLAG] pwn.college{gDFO4ypdY-a1adW1EIoO5L3nkm4.QX1YTN0wCN3AzNzEzW}
```

### New Learnings
I can redirect contents of one file to other and access the output of first file through second.


## Appending output

If you properly redirect in append-mode, the second half will be appended to the first, but if you redirect in truncation mode (>), the second half will overwrite the first and you won't get the flag!

### Solve
**Flag:** pwn.college{UrpelzWmIca8At-NGAnrZENatEK.QX3ATO0wCN3AzNzEzW}

appended /challenge/run to /home/hacker/the-flag then cat /home/hacker/the-flag. 

```bash
/challenge/run >> /home/hacker/the-flag
cat /home/hacker/the-flag
 |
\|/ This is the first half:
 v
pwn.college{UrpelzWmIca8At-NGAnrZENatEK.QX3ATO0wCN3AzNzEzW}
                              ^
     that is the second half /|\
                              |
```

### New Learnings
Directing with >> appends the data not overwrite on the file.


## Redirecting errors

In this challenge, you will need to redirect the output of /challenge/run, like before, to myflag, and the "errors" (in our case, the instructions) to instructions.

### Solve
**Flag:** pwn.college{8C6Dah9hwlJNnA1iHk7ui4OKCRA.QX3YTN0wCN3AzNzEzW}

Redirected the output of /challenge/run to myflag and errors to instructions as /challenge/run > myflag 2> instructions. Then cat myflag to get the flag.

```bash
/challenge/run > myflag 2> instructions
cat myflag
[FLAG] Here is your flag:
[FLAG] pwn.college{8C6Dah9hwlJNnA1iHk7ui4OKCRA.QX3YTN0wCN3AzNzEzW}
```

### New Learnings
2> redirects the standard error FD2 to the given file.


## Redirecting input

In this level, we will practice using /challenge/run, which will require you to redirect the PWN file to it and have the PWN file contain the value COLLEGE!

### Solve
**Flag:** pwn.college{IJQnpnRwrfq4K4_07W4w80Qp8qf.QX4cTO0wCN3AzNzEzW}

Redirected the value COLLEGE to PWN then rediected the /challenge/run to PWN using < as /challenge/run < PWN . 

```bash
echo COLLEGE > PWN
/challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{QB-jH-KXZTXUovEiKVQVB_b8nbA.QXwcTN0wCN3AzNzEzW}
```

### New Learnings
input redirection < . 


## Grepping stored result

In preparation for more complex levels, we want you to:

1. Redirect the output of /challenge/run to /tmp/data.txt.
2. This will result in a hundred thousand lines of text, with one of them being the flag, in 
  /tmp/data.txt.
3. grep that for the flag!

### Solve
**Flag:** pwn.college{UTGw9mv8jqAHSk36y-OIiLaoaBT.QX4EDO0wCN3AzNzEzW}

Redirected the output of /challenge/run to /tmp/data.txt and used grep command to get flag . 

```bash
/challenge/run > /tmp/data.txt

[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
.
.
.
.
.
[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{UTGw9mv8jqAHSk36y-OIiLaoaBT.QX4EDO0wCN3AzNzEzW}
```

### New Learnings
redirection and grepping.


## Grepping live output

Now try it for yourself! /challenge/run will output a hundred thousand lines of text, including the flag. grep for the flag!

### Solve
**Flag:** pwn.college{U3kSEMY3f0sOTZ2B7ZgoEZxH55F.QX5EDO0wCN3AzNzEzW}

grep using | (pipe) operator as /challenge/run | grep pwn.college

```bash
/challenge/run | grep pwn.college

[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
.
.
.
.
.
[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{U3kSEMY3f0sOTZ2B7ZgoEZxH55F.QX5EDO0wCN3AzNzEzW}
```

### New Learnings
grep using | (pipe) operator.


## Grepping errors

Now try it for yourself! /challenge/run will output a hundred thousand lines of text, including the flag. grep for the flag!

### Solve
**Flag:** pwn.college{U3kSEMY3f0sOTZ2B7ZgoEZxH55F.QX5EDO0wCN3AzNzEzW}

redirected standard error to standard output using (2>& 1) then pipe operator to grep flag.

```bash
/challenge/run 2>& 1 | grep pwn.college

[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
.
.
.
.
.
[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{EnDtsnM0158kfJJ7_g_UX4-T8bY.QX1ATO0wCN3AzNzEzW}
```

### New Learnings
(2>& 1) this redirects the standard error to standar output.

## Filtering with grep-v

Use grep -v to filter out all the lines containing "DECOY" and reveal the real flag!

### Solve
**Flag:** pwn.college{MzsYITjl0fibmoWWRlUvHyrybJ2.0FOxEzNxwCN3AzNzEzW}

filtered all the DECOY flags in the /challenge/run using grep -v as /challenge/run | grep -v DECOY .


```bash
/challenge/run | grep -v DECOY
pwn.college{MzsYITjl0fibmoWWRlUvHyrybJ2.0FOxEzNxwCN3AzNzEzW}
```

### New Learnings
filter the file text using grep -v command with pipe operator.


## Duplicating piped data with tee

This process' /challenge/pwn must be piped into /challenge/college, but you'll need to intercept the data to see what pwn needs from you!

### Solve
**Flag:** 

.


```bash

```

### New Learnings



## Process substitution for input 

Use process substitution with diff to compare the outputs of these two programs and find your flag!

### Solve
**Flag:** pwn.college{UV2FjjSmZKtIT63uV35bKXSoq0w.0lNwMDOxwCN3AzNzEzW}

used precess substitution with diff command as diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag) to get the real flag which is in /challenge/print_decoys_and_flag.


```bash
diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
79a80
> pwn.college{UV2FjjSmZKtIT63uV35bKXSoq0w.0lNwMDOxwCN3AzNzEzW}
```

### New Learnings
using process substitution with diff command.


## Writing multiple programs

In this challenge, we have /challenge/hack, /challenge/the, and /challenge/planet. Run the /challenge/hack command, and duplicate its output as input to both the /challenge/the and the /challenge/planet commands!

### Solve
**Flag:** pwn.college{owi9rRVm0wqf53O_kjbQ5Z7D8ef.QXwgDN1wCN3AzNzEzW}

Duplicated the output of /challenge/hack to /challenge/the and /challenge/planet as /challenge/hack | tee >(/challenge/the) | /challenge/planet .


```bash
/challenge/hack | tee >(/challenge/the) | /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{owi9rRVm0wqf53O_kjbQ5Z7D8ef.QXwgDN1wCN3AzNzEzW}
```

### New Learnings
can copy data using >().


## Split-piping stderr and stdout

In this challenge, you have:

• /challenge/hack: this produces data on stdout and stderr
• /challenge/the: you must redirect hack's stderr to this program
• /challenge/planet: you must redirect hack's stdout to this program

### Solve
**Flag:** pwn.college{oFmW6q121yZpyKvJx2UO1iTuXWz.QXxQDM2wCN3AzNzEzW}

Redirected the standard error of /challenge/hack to /challenge/the using 2< then redirected standard output of /challenge/hack to /challenge/planet using >() and | pipe operator because when >() used on /challenge/the it did not redirected the standard error to /challenge/planet.
/challenge/hack 2> >(/challenge/the) | /challenge/planet


```bash
/challenge/hack 2> >(/challenge/the) | /challenge/planet
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{oFmW6q121yZpyKvJx2UO1iTuXWz.QXxQDM2wCN3AzNzEzW}
```

### New Learnings
can redirect stderr to one program and stdout to another using combination of 2>,>() and | operators.


## Named pipes

This challenge will be a simple introduction to FIFOs. You'll need to create a /tmp/flag_fifo file and redirect the stdout of /challenge/run to it. If you're successful, /challenge/run will write the flag into the FIFO!

### Solve
**Flag:** 

.


```bash

```

### New Learnings
