# Bandit Level 13 to 14 Writeup

Author: [Shivam Mishra](https://github.com/7shivamx)

Problem Page: [bandit13](https://overthewire.org/bandit/bandit13) 

## List of Commands Used
```
ls - list files in a directory
ssh  - OpenSSH SSH client (remote login program)
i - parameter to pass a private key 
cat  - concatenate files and print on the standard output
exit - To close the connection to ssh server
```

## Walkthrough
After logging in first of all i ran `ls -lah` to confirm if `sshkey.private` file is present in current working directory. As mentioned on Bandit13 page now i just needed to login as Bandit14 using ssh and private key given to obtain password stored in `/etc/bandit_pass/bandit14` using `cat` command ro write it on standard output. 

## Password
`4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e`

## Bash/Python script to automate the process
```
#!/bin/bash

sshpass -p '8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL' ssh bandit13@bandit.labs.overthewire.org -p 2220 << EOF 

ls -lah
ssh bandit14@localhost -i sshkey.private
cat /etc/bandit_pass/bandit14
EOF
exit
```

## Suggested modifications
Rather than providing location of password file to user, let them to find it on their own.  
