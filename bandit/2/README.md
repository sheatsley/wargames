## Bandit - Level 2
---
>The password for the next level is stored in a file called - located in the
>home directory

Since filenames with spaces, entered as-is, will be interpreted as separate
files, the trick is to quote the filename:
```
bandit2@bandit:~$ cat "spaces in this filename"
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```
