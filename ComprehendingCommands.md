# comprehending commands 

## cat: not the pet , but the command! 

read the flag copied in the flag file in my home directory read it with cat.

### Solve
**Flag:** pwn.college{w0aQXPO8pruu2uWYcBIYOxMyOAy.QXxcTN0wCN3AzNzEzW}

read flag using cat  

```bash
cat flag
pwn.college{w0aQXPO8pruu2uWYcBIYOxMyOAy.QXxcTN0wCN3AzNzEzW}
```

### New Learnings
cat command.  


## Catting absolute paths

access the flag by using cat command by its absolute path /flag.

### Solve
**Flag:** pwn.college{AkFVY9_VuBrJwYSjeQfIqiQXjUl.QX5ETO0wCN3AzNzEzW}

read flag by absolte path /flag using cat  

```bash
cat /flag
pwn.college{AkFVY9_VuBrJwYSjeQfIqiQXjUl.QX5ETO0wCN3AzNzEzW}
```

### New Learnings
read flag by absolute path using cat.  


## more catting practice

access the flag by using cat command by its absolute path in different directory no 'cd' and 'cat flag'.

### Solve
**Flag:** pwn.college{sF2jZx3SkR-v9_N4qwCS769E5bs.QXwITO0wCN3AzNzEzW}

read flag using cat flag from /lib/emacsen-common/flag.

```bash
cat /lib/emacsen-common/flag
pwn.college{sF2jZx3SkR-v9_N4qwCS769E5bs.QXwITO0wCN3AzNzEzW}
```

### New Learnings
read flag by absolute path from different directory without changing current directory using cat.


## grepping for a needle in a haystack

access the flag from a large file using grep command. 

### Solve
**Flag:** pwn.college{8AzR63tvqYHuqXkjR7jOhqOZ-TK.QX3EDO0wCN3AzNzEzW}

find flag using grep 

```bash
grep pwn.college /challenge/data.txt
pwn.college{8AzR63tvqYHuqXkjR7jOhqOZ-TK.QX3EDO0wCN3AzNzEzW}
```

### New Learnings
grep command used for searching contents we need in a large file.


## comparing files

access the flag by comparing two files one has fake flags other has real. 

### Solve
**Flag:** > pwn.college{Yg8ZPz1hi42HiyRACYJMjki0bWP.01MwMDOxwCN3AzNzEzW}

compare file1 by file2 using diff.

```bash
diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
84a85
> pwn.college{Yg8ZPz1hi42HiyRACYJMjki0bWP.01MwMDOxwCN3AzNzEzW}
```

### New Learnings
diff command used for find difference in 2 files. 


## listing files

In this challenge, we've named /challenge/run with some random name! 
List the files in /challenge to find it.

### Solve
**Flag:** > pwn.college{sb8IAnFSNWvYJ5s2fNIkQGokLlR.QX4IDO0wCN3AzNzEzW}

listed files in /challenge then accesed the renamed flag file.

```bash
ls /challenge
2000-renamed-run-9548  DESCRIPTION.md
/challenge/2000-renamed-run-9548
Yahaha, you found me! Here is your flag:
pwn.college{sb8IAnFSNWvYJ5s2fNIkQGokLlR.QX4IDO0wCN3AzNzEzW}
```

### New Learnings
I can list all files under a directory using ls command. 


## touching files

In this level, please create two files: /tmp/pwn and /tmp/college,
and run /challenge/run to get your flag!.

### Solve
**Flag:** > pwn.college{EbZMkfE59n2X7nICC8h5mPvVS7Q.QXwMDO0wCN3AzNzEzW}

created two files pwn and college then used /challenge/run to get the flag.

```bash
cd /tmp
touch pwn
touch college
ls
bin  college  hsperfdata_root  pwn  tmp.TpSOPGOVKK
/challenge/run
Success! Here is your flag:
pwn.college{EbZMkfE59n2X7nICC8h5mPvVS7Q.QXwMDO0wCN3AzNzEzW}
```

### New Learnings
I can create a file in a directory using touch command.


## removing files

this challenge will create a delete_me file in your home directory! Delete it, 
then run /challenge/check, 
which will make sure you've deleted it and then give you the flag!.

### Solve
**Flag:** > pwn.college{8ZnaTvrBet6MYbS1FW0tTJ27WHz.QX2kDM1wCN3AzNzEzW}

deleted a file using rm .

```bash
ls
delete_met
rm delete_me
/challenge/check
Excellent removal. Here is your reward:
pwn.college{8ZnaTvrBet6MYbS1FW0tTJ27WHz.QX2kDM1wCN3AzNzEzW}
```

### New Learnings
I can delete a file in a directory using rm command.


## moving files

This challenge wants you to move the /flag file into /tmp/hack-the-planet (do it)!
When you're done,
run /challenge/check, which will check things out and give the flag to you.

### Solve
**Flag:** pwn.college{UVaPLIv03p9KRa49Au3r6rLdykh.0VOxEzNxwCN3AzNzEzW}

moved /flag to /tmp/hack-the-planet then run /challenge/check to get the flag.

```bash
cd /tmp
mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
/challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{UVaPLIv03p9KRa49Au3r6rLdykh.0VOxEzNxwCN3AzNzEzW}
```

### New Learnings
I can move a file in a directory using mv command.


## hidden files

find the flag, hidden as a dot-prepended file in /.

### Solve
**Flag:** pwn.college{oTHwtRXaNpowPGhk7-CVPkRPBw4.QXwUDO0wCN3AzNzEzW}

moved /flag to /tmp/hack-the-planet then run /challenge/check to get the flag.

```bash
cd /
ls -a
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
ls -a
.           .flag-293013016824097  challenge  home   lib64   mnt  proc  sbin  tmp
..          bin                    dev        lib    libx32  nix  root  srv   usr
.dockerenv  boot                   etc        lib32  media   opt  run   sys   var
cat .flag-293013016824097
pwn.college{oTHwtRXaNpowPGhk7-CVPkRPBw4.QXwUDO0wCN3AzNzEzW}
```

### New Learnings
I can list a 'dot file' that starts with '.' using '-a' flag with 'ls' command as 'ls -a'.


## An epic filesystem quest 

In this challenge, I have hidden the flag! Here, 
you will use ls and cat to follow my breadcrumbs and find it!

### Solve
**Flag:** pwn.college{8Fochw4Grjp1pfRuPkeRvmG0lCo.QX5IDO0wCN3AzNzEzW}

moved /flag to /tmp/hack-the-planet then run /challenge/check to get the flag.

```bash
cd /
ls
.           BRIEF  challenge  flag  lib32   media  opt   run   sys  var
..          bin    dev        home  lib64   mnt    proc  sbin  tmp
.dockerenv  boot   etc        lib   libx32  nix    root  srv   usr
cat BRIEF
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/drivers/s390/cio

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
.
.
.
.
.
.
.
.
cat /usr/lib/debug/.build-id/f8/BLUEPRINT-TRAPPED
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{8Fochw4Grjp1pfRuPkeRvmG0lCo.QX5IDO0wCN3AzNzEzW}

```

### New Learnings
practice of 'cd' , 'cat' , 'ls' , 'ls-a'.















