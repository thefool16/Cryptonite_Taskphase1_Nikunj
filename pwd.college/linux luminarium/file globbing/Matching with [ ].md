```
Connected!
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run --Look: file_[bash]
Error: you called this command with more than 1 argument (pre-globbing)! Please
call me with one argument.
hacker@globbing~matching-with-:/challenge/files$ Look: file_[bash]
ssh-entrypoint: Look:: command not found
hacker@globbing~matching-with-:/challenge/files$ echo Look: file_[bash]
Look: file_a file_b file_h file_s
hacker@globbing~matching-with-:/challenge/files$ /challenge/run
Error: you did not use a square bracket glob...
hacker@globbing~matching-with-:/challenge/files$ /challenge/runbecho Look: file_[bash]
ssh-entrypoint: /challenge/runbecho: No such file or directory
hacker@globbing~matching-with-:/challenge/files$ /challenge/run echo Look: file_[bash]
Error: you called this command with more than 1 argument (pre-globbing)! Please
call me with one argument.
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{0PDhM4vhWDRis5GogCA5hJmFJSY.dNjM4QDLyIjN0czW}

i founded all the files and understood how [ ] worked but have to think some more how to get the flag
```
