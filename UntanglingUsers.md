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
