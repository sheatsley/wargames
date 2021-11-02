## Bandit - Level 5
---
>The password for the next level is stored in a file somewhere under the inhere
>directory and has all of the following properties:
>
>   human-readable
>   1033 bytes in size
>   not executable

This one had me thinking for a little bit. Some important facts about this
environment:

1. There were _a lot_ of files (prohibits manual search)
2. There were subdirectories (requires recursive approach)
3. _Some files are hidden_ (mandates using `find`)

My first attempt `du -a -b **/* | grep 1033` failed to check hidden files.
While the `find` manpage doesn't mention "hidden" directly, executing it showed
that it also finds hidden files. The "human-readable" and "not executable"
might be useful for alternative strategies, but `du` with `-a` (show statistics
for files as well as directories) and `-b` (print results in bytes) gets the
job done:
```
bandit5@bandit:~/inhere$ find . | du -a -b | grep 1033
1033	./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```
