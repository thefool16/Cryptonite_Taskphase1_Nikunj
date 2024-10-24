
```
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak

Loaded 1 password hash (crypt, generic crypt(3) [?/64])

Press 'q' or Ctrl-C to abort, almost any other key for status

0g 0:00:00:06 69% 1/3 0g/s 286.5p/s 286.5c/s 286.5C/s Z99999E..1z999991

aardvark         (zardus)

1g 0:00:00:20 100% 2/3 0.04916g/s 286.2p/s 286.2c/s 286.2C/s Johnson..buzz

Use the "--show" option to display all of the cracked passwords reliably

Session completed

hacker@users~cracking-passwords:~$ su zardus

Password:

zardus@users~cracking-passwords:/home/hacker$ /challenge/run

Congratulations, you have become Zardus! Here is your flag:

pwn.college{wjmCEsxKaTUI9my8jh1RC_7yqgS.ddTN0UDLyIjN0czW}
