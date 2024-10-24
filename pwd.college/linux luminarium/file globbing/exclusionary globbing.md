```
thefool@DESKTOP-GUJVLIO:~$ ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]
Your expansion did not expand to the requested files (amazing beautiful
challenging delightful educational fantastic great happy incredible jovial kind
laughing magical optimistic queenly radiant splendid thrilling uplifting
victorious xenial youthful zesty).
Instead, it expanded to:
[!pwn]
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{YPDso1aYGg2BZhCxdocaZycTQ61.dZjM4QDLyIjN0czW}

just removed the files starting with pwn using [] and ! used * for expansion
```
