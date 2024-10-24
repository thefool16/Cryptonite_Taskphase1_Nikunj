```
hacker@permissions~changing-file-ownership:/$ ls -l

total 80

lrwxrwxrwx    1 root root    7 May 30 02:03 bin -> usr/bin

drwxr-xr-x    1 root root 4096 Apr 15  2020 boot

drwxr-xr-x    1 root root 4096 Oct 20 09:32 challenge

drwxr-xr-x    6 root root  380 Oct 20 09:32 dev

drwxr-xr-x    1 root root 4096 Oct 20 09:32 

-r--------    1 root root   58 Oct 20 09:32 flag

drwxr-xr-x    1 root root 4096 Oct  4 23:03 home

lrwxrwxrwx    1 root root    7 May 30 02:03 lib -> usr/lib

lrwxrwxrwx    1 root root    9 May 30 02:03 lib32 -> usr/lib32

lrwxrwxrwx    1 root root    9 May 30 02:03 lib64 -> usr/lib64

lrwxrwxrwx    1 root root   10 May 30 02:03 libx32 -> usr/libx32

drwxr-xr-x    1 root root 4096 May 30 02:03 media

drwxr-xr-x    1 root root 4096 May 30 02:03 mnt

drwxr-xr-x    4 root root 4096 Sep  6 16:53 nix

drwxr-xr-x    1 root root 4096 Sep  6 16:42 opt

dr-xr-xr-x 2166 root root    0 Oct 20 09:32 proc

drwx------    1 root root 4096 Sep  6 16:43 root

drwxr-xr-x    1 root root 4096 Oct 20 09:32 run

lrwxrwxrwx    1 root root    8 May 30 02:03 sbin -> usr/sbin

drwxr-xr-x    1 root root 4096 May 30 02:03 srv

dr-xr-xr-x   13 root root    0 Sep 15 22:45 sys

drwxrwxrwt    1 root root 4096 Oct 20 09:32 tmp


drwxr-xr-x    1 root root 4096 Sep  6 16:25 usr
drwxr-xr-x    1 root root 4096 May 30 02:07 var

hacker@permissions~changing-file-ownership:/$ chown hacker flag

hacker@permissions~changing-file-ownership:/$ ls -l
total 80
lrwxrwxrwx    1 root   root    7 May 30 02:03 bin -> usr/bin
drwxr-xr-x    1 root   root 4096 Apr 15  2020 boot
drwxr-xr-x    1 root   root 4096 Oct 20 09:32 challenge
drwxr-xr-x    6 root   root  380 Oct 20 09:32 dev
drwxr-xr-x    1 root   root 4096 Oct 20 09:32 etc

-r--------    1 hacker root   58 Oct 20 09:32 flag

drwxr-xr-x    1 root   root 4096 Oct  4 23:03 home
lrwxrwxrwx    1 root   root    7 May 30 02:03 lib -> usr/lib
lrwxrwxrwx    1 root   root    9 May 30 02:03 lib32 -> usr/lib32
lrwxrwxrwx    1 root   root    9 May 30 02:03 lib64 -> usr/lib64
lrwxrwxrwx    1 root   root   10 May 30 02:03 libx32 -> usr/libx32
drwxr-xr-x    1 root   root 4096 May 30 02:03 media
drwxr-xr-x    1 root   root 4096 May 30 02:03 mnt
drwxr-xr-x    4 root   root 4096 Sep  6 16:53 nix
drwxr-xr-x    1 root   root 4096 Sep  6 16:42 opt
dr-xr-xr-x 2162 root   root    0 Oct 20 09:32 proc
drwx------    1 root   root 4096 Sep  6 16:43 root
drwxr-xr-x    1 root   root 4096 Oct 20 09:32 run
lrwxrwxrwx    1 root   root    8 May 30 02:03 sbin -> usr/sbin
drwxr-xr-x    1 root   root 4096 May 30 02:03 srv
dr-xr-xr-x   13 root   root    0 Sep 15 22:45 sys
drwxrwxrwt    1 root   root 4096 Oct 20 09:32 tmp
drwxr-xr-x    1 root   root 4096 Sep  6 16:25 usr
drwxr-xr-x    1 root   root 4096 May 30 02:07 var


hacker@permissions~changing-file-ownership:/$ /challenge/run

I have given you access to use the 'chown' command. Use it to enable the flag
to be read!

hacker@permissions~changing-file-ownership:/$ cat /flag

pwn.college{gcxMKhNVLbyc68Bv011BwwMFZWa.dFTM2QDLyIjN0czW}

```
