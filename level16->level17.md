Level Goal

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

Use ssh command and password we got earlier to login as user bandit16 to host

<img width="981" height="390" alt="image" src="https://github.com/user-attachments/assets/5e4397c2-c85c-495e-8c84-f4d1ae271ea4" />

Step 1: Confirm current password
cat /etc/bandit_pass/bandit16

Step 2: Scan for open ports

Scan ports 31000–32000 on localhost.

nmap localhost -p 31000-32000

Step 3: Identify open ports

Open ports found:

31046
31518
31691
31790
31960

Step 4: Perform service/version scan on open ports

nmap localhost -p 31046,31518,31691,31790,31960 -sV -T4

Step 5: Analyze scan results

Important finding:

31790/tcp open ssl/unknown

This port supports SSL and is not a simple echo service.

Step 6: Try SSL connection on the correct port

ncat localhost 31790 --ssl

Step 7: Send the current password

Paste the bandit16 password and press Enter.

XXXXXXXXXXXXXX

Step 8:

Output:

Correct!
-----BEGIN RSA PRIVATE KEY-----
...
-----END RSA PRIVATE KEY-----


This key is used to log in to bandit17.

Step 9:Copy the entire key (including BEGIN and END lines) into a key file in local machiene

Step 11: Set correct permissions on the key

chmod 600 ssh_key

Step 12: Verify permissions

ls -l ssh_key

Step 13: Login to bandit17 using the private key

ssh -i ssh_key bandit17@bandit.labs.overthewire.org -p 2220

Screenshots:

<img width="946" height="400" alt="image" src="https://github.com/user-attachments/assets/159decda-957e-4065-8647-d547c339dc09" />

<img width="1103" height="706" alt="image" src="https://github.com/user-attachments/assets/af23a9e0-8e61-4b4c-9616-edd9d294126c" />

<img width="792" height="689" alt="image" src="https://github.com/user-attachments/assets/b6369606-7f17-4c3d-94fb-dfe0559cabbb" />

<img width="1310" height="377" alt="image" src="https://github.com/user-attachments/assets/b6656719-7307-4577-9b93-844dcc78e95a" />

<img width="941" height="396" alt="image" src="https://github.com/user-attachments/assets/a300d6c0-7f41-4ef7-8934-6bde59297112" />










