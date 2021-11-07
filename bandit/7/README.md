## Bandit - Level 7
---
>The password for the next level is stored in the file data.txt next to the
>word millionth

This challenge appears to transition from focusing on searching for files, to
searching within files (i.e., `grep`):
```
bandit7@bandit:~$ grep millionth < data.txt
millionth	cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```
