Connected

hacker@processes~listing-processes:~$ ps -ef

UID          PID    PPID  C STIME TTY          TIME CMD

root           1       0  0 18:48 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /ru

root           7       1  0 18:48 ?        00:00:00 /run/dojo/bin/sleep 6h

root          68       1  0 18:48 ?        00:00:00 /challenge/325-run-2948

root          72      68  0 18:48 ?        00:00:00 sleep 6h

hacker        73       0  0 18:48 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint

hacker        90       0  0 18:48 pts/1    00:00:00 /run/dojo/bin/ssh-entrypoint

hacker       107      90  0 18:48 pts/1    00:00:00 ps -ef

hacker@processes~listing-processes:~$ /challenge/325-run-2948

Yahaha, you found me! Here is your flag:

pwn.college{8cXlOZXV8ZhuHde086nXLAusrOa.dhzM4QDLyIjN0czW}

Now I will sleep for a while (so that you could find me with 'ps')

ran the ps ef command to find the flag file and then ran the founded file
