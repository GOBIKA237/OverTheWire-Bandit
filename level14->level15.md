Level Goal

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost

Use ssh command and the password we got earlier to connect to host as bandit14

Step 1: Confirm the current user

You are logged in as bandit14.

whoami

Step 2: Read the current level password

The password for bandit14 is stored in the system directory.

cat /etc/bandit_pass/bandit14

Step 3: Connect to the local service

A service is listening on localhost port 30000.

nc localhost 30000

Step 4: Send the password

Paste the bandit14 password and press Enter.

MU4WWeTyJk8ROof1qqmcBPahLh7lDCPvS

Step 5: Receive the next password

Output should look like this:

<img width="476" height="130" alt="image" src="https://github.com/user-attachments/assets/a9ed1ace-e35b-4095-ab2e-2c39c6021990" />

