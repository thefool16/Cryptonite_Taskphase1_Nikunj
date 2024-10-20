hacker@permissions~fun-with-groups-names:~$ id

uid=1000(hacker) gid=1000(grp31730) groups=1000(grp31730)


hacker@permissions~fun-with-groups-names:~$ chgrp grp31730

chgrp: missing operand after ‘grp31730’

Try 'chgrp --help' for more information.

hacker@permissions~fun-with-groups-names:~$ chgrp grp31730 /flag

hacker@permissions~fun-with-groups-names:~$ cat /flag

pwn.college{8oeJyhU-ZJxOKqRYAxFZlwQFz2Z.dJzNyUDLyIjN0czW}
