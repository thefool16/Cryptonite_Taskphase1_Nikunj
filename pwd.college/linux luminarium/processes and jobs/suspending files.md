hacker@processes~suspending-processes:~$ /challenge/run

I'll only give you the flag if there's already another copy of me running in

this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD

root         109      65  0 19:13 pts/1    00:00:00 bash /challenge/run

root         111     109  0 19:13 pts/1    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can

background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!

^Z

[1]+  Stopped                 /challenge/run

hacker@processes~suspending-processes:~$ /challeng/run

ssh-entrypoint: /challeng/run: No such file or directory

hacker@processes~suspending-processes:~$ /challenge/run

I'll only give you the flag if there's already another copy of me running in

this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD

root         109      65  0 19:13 pts/1    00:00:00 bash /challenge/run

root         117      65  0 19:13 pts/1    00:00:00 bash /challenge/run

root         119     117  0 19:13 pts/1    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:

pwn.college{AqWMKqjb1vw3gKcTPWu3rKNXGSX.dVDN4QDLyIjN0czW}
