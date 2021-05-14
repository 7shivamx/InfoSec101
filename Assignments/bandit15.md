# Bandit Level 15 to 16 Writeup

Author: [Shivam Mishra](https://github.com/7shivamx)

Problem Page: [bandit15](https://overthewire.org/bandit/bandit15)

## List of Commands Used
```
ls - list files in a directory
cd - change directory
openssl - OpenSSL commandline tool for using the various cryptography functions of OpenSSL's crypto library from the shell
s_client - implements a generic SSL/TLS client to establish a transparent connection to a remote server speaking SSL/TLS
reading material offered we can see which steps to take next
```

## Walkthrough
For this level I looked for `openssl` and `s_client` reading material offered to see which steps to take next after logging in using ssh. After connecting to `port 30001`on localhost using encryption we just need to enter Bandit15’s password to obtain Bandit16’s password.

## Password
`cluFn7wTiGryunymYOu4RcffSxQluehd`

## Bash/Python script to automate the process
```
#!/bin/bash

sshpass -p "BfMYroe26WYalil77FoDi9qh59eK5xNr" ssh bandit15@bandit.labs.overthewire.org -p 2220 << EOF 

openssl s_client -connect localhost:30001
BfMYroe26WYalil77FoDi9qh59eK5xNr
EOF
exit
```
## Suggested modifications [Optional]

