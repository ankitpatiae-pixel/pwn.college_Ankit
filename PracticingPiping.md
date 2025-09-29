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

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.

[FLAG] Here is your flag:
[FLAG] pwn.college{gDFO4ypdY-a1adW1EIoO5L3nkm4.QX1YTN0wCN3AzNzEzW}
```

### New Learnings
I can redirect contents of one file to other and access the output of first file through second.



