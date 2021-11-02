## Bandit - Level 0
---
>The goal of this level is for you to log into the game using SSH. The host to
>which you need to connect is bandit.labs.overthewire.org, on port 2220. The
>username is bandit0 and the password is bandit0. Once logged in, go to the
>Level 1 page to find out how to beat Level 1.

Other than standard  `ssh` access, the only important detail is _"... on port
2220"_, which, from the `ssh` `man` page can be specified with `-p --port`.

>The password for the next level is stored in a file called readme located in
>the home directory. Use this password to log into bandit1 using SSH. Whenever
>you find a password for a level, use SSH (on port 2220) to log into that level
>and continue the game.

We can read the file to `STDOUT` via:
```
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```
