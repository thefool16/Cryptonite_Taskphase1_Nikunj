```
hacker@processes~killing-processes:~$  ps -ef | grep run

root  1       0  0 18:54 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /run/dojo/bin/sleep 6h

root           7       1  0 18:54 ?        00:00:00 /run/dojo/bin/sleep 6h

hacker        73      71  0 18:54 ?        00:00:00 /challenge/dont_run

hacker        75       0  0 18:54 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint

hacker        81       0  0 18:54 pts/1    00:00:00 /run/dojo/bin/ssh-entrypoint

hacker       114      81  0 18:55 pts/1    00:00:00 grep --color=auto run

hacker@processes~killing-processes:~$ ps -e | grep run

      7 ?        00:00:00 /run/dojo/bin/s
      
hacker@processes~killing-processes:~$ kill 73

hacker@processes~killing-processes:~$

hacker@processes~killing-processes:~$ ps -ef | grep run

root           1       0  0 18:54 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /run/dojo/bin/sleep 6h

root           7       1  0 18:54 ?        00:00:00 /run/dojo/bin/sleep 6

hacker        75       0  0 18:54 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint

hacker        81       0  0 18:54 pts/1    00:00:00 /run/dojo/bin/ssh-entrypoint

hacker       118      81  0 18:57 pts/1    00:00:00 grep --color=auto run

hacker@processes~killing-processes:~$ /challenge/run

Great job! Here is your payment:

pwn.college{IqULfJe8eZy3p66ykHQPNyKy4X2.dJDN4QDLyIjN0czW}
```

