# Data Manipulation

## Translating characters

Now, you try it! In this level, /challenge/run will print the flag
but will swap the casing of all characters (e.g., A will become a and vice-versa).
Can you undo it with tr and get the flag?

### Solve
**Flag:** pwn.college{Y8O4SVsHCl5fIs8dcQ0qDiXhz9g.QX0YTN0wiM5AzNzEzW} 
 

```bash


```

### New Learnings


## Deleting characters

 Now you give it a try. I'll intersperse some decoy characters (specifically: ^ and %)
 among the flag characters. Use tr -d to remove them!

### Solve
**Flag:** pwn.college{sf-qDBK0p3pFoXjHNn2JD2l7_i9.0FNxEzNxwCN3AzNzEzW}
deleted the unnecessary characters in string using tr -d as tr -d %^  

```bash
/challenge/run
Your character-stuffed flag:
p%w^%n%.^c%o^%lle^g^e%{^%s%f-^q^%D^%BK0^%p%3%p^F^%o^Xj^%H^%N^%n%2^J^D^2%l%7%_^%i%9%.%0F%N^x^%Ez^N^%x^%w^%C%N%3%A%zN%z%E^z^W^}^%%
 echo p%w^%n%.^c%o^%lle^g^e%{^%s%f-^q^%D^%BK0^%p%3%p^F^%o^Xj^%H^%N^%n%2^J^D^2%l%7%_^%i%9%.%0F%N^x^%Ez^N^%x^%w^%C%N%3%A%zN%z%E^z^W^}^%% | tr -d %^
pwn.college{sf-qDBK0p3pFoXjHNn2JD2l7_i9.0FNxEzNxwCN3AzNzEzW}
```

### New Learnings
can delete characters like '!@#$%^&' using tr -d command.




