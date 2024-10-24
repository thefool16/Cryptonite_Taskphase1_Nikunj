```
Connected!
hacker@man~reading-manuals:~$ man challenge

CHALLENGE(1)                                      Challenge Commands                                     CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --vwlesu NUM
              print the flag if NUM is 034

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)
hacker@man~reading-manuals:~$ /challenge/challenge --vwlesu 034
Correct usage! Your flag: pwn.college{YBvwVXleGLsuNHYG0UvosA3cPij.dRTM4QDLyIjN0czW}


i gave the man command as instruted finded the clue and got the flag
```
