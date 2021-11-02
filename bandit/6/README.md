## Bandit - Level 6
---
>The password for the next level is stored somewhere on the server and has all
>of the following properties:
>
>   owned by user bandit7
>   owned by group bandit6
>   33 bytes in size

As I mentioned in the prior challenge, there could be other strategies that
involve parsing for user and group; this was such a challenge. Understanding
`find` was the key here, specifically the `-user` and `-group` options. Since I
did not have permissions to read many directories, redirecting `STDERR` to
`/dev/null` made parsing the results easy:
```
bandit6@bandit:/$ find . -user bandit7 -group bandit6 2>/dev/null
./var/lib/dpkg/info/bandit7.password
bandit6@bandit:/$ du -b var/lib/dpkg/info/bandit7.password
33	var/lib/dpkg/info/bandit7.password
bandit6@bandit:/$ cat var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```
