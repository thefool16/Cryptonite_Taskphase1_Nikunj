```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee xyz| /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat xyz
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "UxVVHgZF"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret [UxVVHgZF]
Processing...
You must pipe the output of /challenge/pwn into /challenge/college (or 'tee'
for debugging).
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret [UxVVHgZF]| /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret ["UxVVHgZF"]| /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret UxVVHgZF | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{UxVVHgZFKXZP_WMKfB8OZ2YJoPB.dFjM5QDLyIjN0czW}



REPORT :- i would say this is the most confusing challenge till now first in this challenge i directed the output of certain files using tee to 2 files and cat the files that i have copied the data to get the secret code and run the piped command 
with the secret code to get the flag
```
