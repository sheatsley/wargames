## Bandit - Level 10
---
>The password for the next level is stored in the file data.txt, which contains
>base64 encoded data

This challenge was to introduce `base64` for decoding base64-encoded data. The
password was simply:
```
bandit10@bandit:~$ base64 -d data.txt
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```
