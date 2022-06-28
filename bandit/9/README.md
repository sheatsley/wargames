## Bandit - Level 9
---
>The password for the next level is stored in the file data.txt in one of the
>few human-readable strings, preceded by several ‘=’ characters.

This challenge was aimed towards learning `strings`. `strings` prints the
printable character sequences that are at least `n` characters long (defaulting
to 4). Thus, the password was found by simply piping the output of calling
`strings` with `data.txt` to `grep` with "several" `=` characters.
```
bandit9@bandit:~$ strings data.txt | grep =====
========= the*2i"4
========= password
Z)======== is
&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```
