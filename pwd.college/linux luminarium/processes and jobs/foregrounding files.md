```
Connected!

hacker@processes~foregrounding-processes:~$ /challenge/run

To pass this level, you need to suspend me, resume the suspended process in the

background, and *then* foreground it without re-suspending it! You can

background me with Ctrl-Z (and resume me in the background with 'bg') or, if

you're not ready to do that for whatever reason, just hit Enter and I'll exit!

^Z

[1]+  Stopped                 /challenge/run

hacker@processes~foregrounding-processes:~$ bg

[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably

overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times

to scroll this text out. After that, resume me into the foreground with 'fg';

I'll wait.

hacker@processes~foregrounding-processes:~$ fg

/challenge/run

YES! Great job! I'm now running in the foreground. Hit Enter for your flag!


pwn.college{MoatB0jpi2-3EigplRCOvbBWOgc.dhDN4QDLyIjN0czW}
```
