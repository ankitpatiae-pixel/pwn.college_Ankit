# Pondering Paths

## The root 
invoke a program by providing its path on the command line.

### Solve
**Flag:** pwn.college{IJQnpnRwrfq4K4_07W4w80Qp8qf.QX4cTO0wCN3AzNzEzW}

written /pwn  

```bash
/pwn
BOOM!!!
Here is your flag:
pwn.college{IJQnpnRwrfq4K4_07W4w80Qp8qf.QX4cTO0wCN3AzNzEzW}
```

### New Learnings
absolute path.


## Program and absolute paths 

execute the run file that is in the challenge directory that is, in turn, in the / directory.

### Solve
**Flag:** pwn.college{IZldGJ2tgyUBEY4lFlqlurZ4hmA.QX1QTN0wCN3AzNzEzW}

accessed the run file in the challenge directory which is in / directory.

```bash
/challenge/run

Correct!!!

/challenge/run is an absolute path! Here is your flag:

pwn.college{IZldGJ2tgyUBEY4lFlqlurZ4hmA.QX1QTN0wCN3AzNzEzW}
```

### New Learnings
file inside a directory.


## Position thy self

execute the /challenge/run program from a specific path '/'.

### Solve
**Flag:** pwn.college{gL_GCSWzFujGU6u7TWVY9PcRqzx.QX2QTN0wCN3AzNzEzW}

first change the directory from ~ to / then accessed the run file in challenge directory. 

```bash
cd /
/challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{gL_GCSWzFujGU6u7TWVY9PcRqzx.QX2QTN0wCN3AzNzEzW}
```

### New Learnings
'~' shows the current path and 'cd' to change the directory to '/'.


## Position elsewhere

execute the /challenge/run program from a specific path '/home'

### Solve
**Flag:** pwn.college{I5v-6imfPtq79P8s0FstAfC3Y1g.QX3QTN0wCN3AzNzEzW}

first change the directory from ~ to /home then accessed the run file in challenge directory. 

```bash
cd /
/challenge/run
Incorrect...
You are not currently in the /home directory.
Please use the `cd` utility to change directory appropriately.
cd /home
/challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{I5v-6imfPtq79P8s0FstAfC3Y1g.QX3QTN0wCN3AzNzEzW}
```

### New Learnings
access a file from different directory '/home'.


## Position yet elsewhere

execute the /challenge/run program from a specific directory '/tmp'

### Solve
**Flag:** pwn.college{c_TF2XYGHX9zd1DTrXjL64NJPeL.QX4QTN0wCN3AzNzEzW}

first change the directory from ~ to /tmp then /challenge/run.

```bash
cd /
/challenge/run
Incorrect...
You are not currently in the /tmp directory.
Please use the `cd` utility to change directory appropriately.
cd /tmp
/challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{c_TF2XYGHX9zd1DTrXjL64NJPeL.QX4QTN0wCN3AzNzEzW}
```

### New Learnings
access a file from different path '/tmp'.


## implicit relative paths , from '/'

run /challenge/run using a relative path while having a current working directory of '/' .

### Solve
**Flag:** pwn.college{sQ_Cxxldrj1CBSLFL-gCc7adDT6.QX5QTN0wCN3AzNzEzW}

first change the directory from ~ to / then challenge/run .

```bash
cd /
challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{sQ_Cxxldrj1CBSLFL-gCc7adDT6.QX5QTN0wCN3AzNzEzW}
```

### New Learnings
access a file by using relative path.


## explicit relative paths , from '/'

run /challenge/run explicitly using a '.' in my relative path while having a current working directory of '/' 

### Solve
**Flag:** pwn.college{EPrd1wdxnZDwCIyRNNXwcSKjnuy.QXwUTN0wCN3AzNzEzW}

first change the directory from ~ to / then ./challenge/run

```bash
cd /
./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{EPrd1wdxnZDwCIyRNNXwcSKjnuy.QXwUTN0wCN3AzNzEzW}
```

### New Learnings
access a file explicitly by using '.' in relative path.


## implicit relative paths 

This challenge will need you to run it from the /challenge directory . Explicitly use relative paths to launch 'run'.

### Solve
**Flag:** pwn.college{Y4MnMfOkYSqy2gjEpds43HtXYtb.QXxUTN0wCN3AzNzEzW}

first change the directory from ~ to /challenge then ./run

```bash
cd /challenge
./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{Y4MnMfOkYSqy2gjEpds43HtXYtb.QXxUTN0wCN3AzNzEzW}
```

### New Learnings
access a file explicitly by using '.' in relative path. from /challenge directory.


## home sweet home 

In this challenge, /challenge/run will write a copy of the flag to any file you specify as an argument on the commandline.

### Solve
**Flag:** pwn.college{kyAew6qczQzirsbwy7XuLMVIdO4.QXzMDO0wCN3AzNzEzW}

copying flag from /challenge/run and writting on specific file

```bash
/challenge/run ~/~
Writing the file to /home/hacker/~!
... and reading it back to you:
pwn.college{kyAew6qczQzirsbwy7XuLMVIdO4.QXzMDO0wCN3AzNzEzW}
```

### New Learnings
copying flag to any specific file as an argument on the commandline.



