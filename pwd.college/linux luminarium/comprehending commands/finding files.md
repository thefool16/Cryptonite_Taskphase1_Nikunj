```
Connected!
hacker@commands~finding-files:~$ find -name flag
hacker@commands~finding-files:~$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/tmp/tmp.G9qthVCks5’: Permission denied
/usr/local/share/jupyter/nbconvert/templates/compatibility/flag
/usr/local/share/radare2/5.9.5/flag
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/7/task/7/fd’: Permission denied
find: ‘/proc/7/task/7/fdinfo’: Permission denied
find: ‘/proc/7/task/7/ns’: Permission denied
find: ‘/proc/7/fd’: Permission denied
find: ‘/proc/7/map_files’: Permission denied
find: ‘/proc/7/fdinfo’: Permission denied
find: ‘/proc/7/ns’: Permission denied
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/opt/radare2/libr/flag
/nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
/nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
hacker@commands~finding-files:~$ cat /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
cat: /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cat /opt/radare2/libr/flag
cat: /opt/radare2/libr/flag: Is a directory
hacker@commands~finding-files:~$ cat /nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
cat: /nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cat /nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
cat: /nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag: Is a directory
hacker@commands~finding-files:~$ cd /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib
hacker@commands~finding-files:/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib$ ls
__init__.py     atexit.py    dynelf.py       fmtstr.py            log.py           rop             ui.py
__pycache__     commandline  elf             gdb.py               memleak.py       runner.py       update.py
abi.py          config.py    encoders        gdb_api_bridge.py    pep237.py        shellcraft      useragents.py
adb             constants    exception.py    gdb_faketerminal.py  protocols        term            util
args.py         context      filepointer.py  internal             qemu.py          testexample.py  version.py
asm.py          data         filesystem      lexer.py             regsort.py       timeout.py
atexception.py  device.py    flag            libcdb.py            replacements.py  tubes
hacker@commands~finding-files:/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib$ cat flag
cat: flag: Is a directory
hacker@commands~finding-files:/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib$ cd ~
hacker@commands~finding-files:~$ cat /usr/local/share/jupyter/nbconvert/templates/compatibility/flag
hacker@commands~finding-files:~$ cat /usr/local/share/jupyter/nbconvert/templates/compatibility/flag
pwn.college{QtFtcDsYs4SLIxSuMJ1a4zOw8dd.dJzM4QDLyIjN0czW}hacker@commands~finding-files:~$
```



we searched for all the flag files in the system and tried to read the flag file one by one 