# Untangling Users

## Becoming root with su

THIS challenge (and only this challenge) does have a root password. That password is hack-the-planet, 
and you must provide it to su to become root! Go do that, and read the flag!

### Solve
**Flag:** pwn.college{gMIhGY6_5sOyCpZXDgUZMUiTlch.QX1UDN1wCN3AzNzEzW}
 

```bash
su
password:hack-the-planet
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{gMIhGY6_5sOyCpZXDgUZMUiTlch.QX1UDN1wCN3AzNzEzW}
```

### New Learnings
using root access."su" substitute user command.


## Other users with su

In this level, you must switch to the zardus user and then run /challenge/run. Zardus' password is dont-hack-me. Good luck!

### Solve
**Flag:** pwn.college{ADIlXh_lKx3rC2iePbrV9963Koy.QX2UDN1wCN3AzNzEzW}

changing user from hacker to zardus as su zardus and then its password dont-hack-me.

```bash
su zardus
password:dont-hack-me
/challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{ADIlXh_lKx3rC2iePbrV9963Koy.QX2UDN1wCN3AzNzEzW}
```

### New Learnings
using su command to change user.


## Cracking passwords

This level simulates this story, giving you a leak of /etc/shadow (in /challenge/shadow-leak). Crack it (this could take a few minutes), su to zardus, and run /challenge/run to get the flag!

### Solve
**Flag:**  pwn.college{ghJKhcuyj1sTgQtmlMqXJDAafXo.QX3UDN1wCN3AzNzEzW}

used john the rippler method to find the password as john shadow-leak

```bash
cd /challenge
john shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04814g/s 280.3p/s 280.3c/s 280.3C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed

su zardus
Password:aardvark

/challenge/run

Congratulations, you have become Zardus! Here is your flag:
pwn.college{ghJKhcuyj1sTgQtmlMqXJDAafXo.QX3UDN1wCN3AzNzEzW}
```

### New Learnings
john the rippler method to find password.


## using sudo

In this level, we will give you sudo access, and you will use it to read the flag. Nice and easy!

### Solve
**Flag:**  pwn.college{ghJKhcuyj1sTgQtmlMqXJDAafXo.QX3UDN1wCN3AzNzEzW}

used sudo to get root access and then cat the flag in not-the-flag file as sudo cat not-the-flag

```bash
ls
sudo cat not-the-flag
pwn.college{ogygXGqdwEOfSuEjFnVhcmgdapa.QX4UDN1wCN3AzNzEzW}
```

### New Learnings
sudo command.sudo defaults to running a command as root.
