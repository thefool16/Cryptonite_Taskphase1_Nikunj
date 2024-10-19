Connected!

hacker@processes~process-exit-codes:~$ /challenge/get-code

Exiting with an error code!


hacker@processes~process-exit-codes:~$ echo $?

141

hacker@processes~process-exit-codes:~$ /challenge/submit-code --141

Incorrect... Make sure to use $? immediately after running /challenge/get-code.

Your shell will overwrite the $? variable with the exit value of any other

command you run!

hacker@processes~process-exit-codes:~$ /challenge/submit-code 141

CORRECT! Here is your flag:

pwn.college{0_WkLmPTHod7HBuZfso4_htAsdu.dljN4UDLyIjN0czW}
