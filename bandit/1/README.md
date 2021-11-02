## Bandit - Level 1
---
>The password for the next level is stored in a file called - located in the
>home directory

The trick here is to recognize `-` is the standard syntax to interpret CL
arguments. Thus, trying `cat -` will hang (awaiting input from `STDIN`, since
`-` is interpreted as an argument).

So, one way to tackle this is to simply reference it by its full path:
```
bandit1@bandit:~$ cat /home/bandit1/-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```
