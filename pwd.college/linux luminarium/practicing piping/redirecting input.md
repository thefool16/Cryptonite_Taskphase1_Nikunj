```
hacker@piping~redirecting-input:~$ echo COLLEGE > pwn
hacker@piping~redirecting-input:~$ /challenge/run < pwn
You must redirect a file called PWN into my standard input! You are currently
redirecting pwn, which is not PWN.
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{48t9D9krVb-FRWWWSYRmPk1Q6N_.dBzN1QDLyIjN0czW}
```
