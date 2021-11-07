## Bandit - Level 8
---
>The password for the next level is stored in the file data.txt and is the only
>line of text that occurs only once

This challenge was focused on learning `uniq`. Simply using the option `-u`,
which causes `uniq` to "only print unique lines" did not work. The note at the
bottom of the manpage clarified why:

>Note: 'uniq' does not detect repeated lines unless they are adjacent.  You may
>want to sort the  input  first, or use 'sort -u' without 'uniq'.  Also,
>comparisons honor the rules specified by 'LC_COLLATE'.

Thus, after using `sort` to sort `data,txt`, we can pipe the output into
`uniq -u` to obtain the password:
```
bandit8@bandit:~$ sort data.txt | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```
