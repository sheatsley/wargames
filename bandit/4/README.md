## Bandit - Level 4
---
>The password for the next level is stored in the only human-readable file in
>the inhere directory. Tip: if your terminal is messed up, try the “reset”
>command.

Same trick as one of the prior lessons; filenames that begin with `-` (with a
subsequent character) will be interpreted as an argument. We can print the files
one by one, or we can just use the wildcard `*`:
```
bandit4@bandit:~/inhere$ cat ./-file0*
�/`2ғ�%��rL~5�g��� �������p,k�;��r*��	�.!��C��J	�dx,�e�)�#��5��
                                                                       ��p��V�_���ׯ�mm�����h!TQO�`�4"aל�߂phT��,�Ai�4�ו$�?��r�l$�?h�9('���!y�e�#�x�O��=�ly���~��A�f����-E�{���m�����ܗMkoReBOKuIDDepwhWk7jZC0RTdopnAYKh
�T�?�i��j��îP�F�l�n��J����{��@�e�0$�in=��_b�5FA�P7sz��gNbandit4@bandit:~/inhere$
```
