Level Goal

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think

Use ssh and password we got earlier and login to host in two different terminals

<img width="1415" height="624" alt="image" src="https://github.com/user-attachments/assets/7000a10f-6063-4a89-8e79-c0546abe95b5" />

<img width="1142" height="493" alt="image" src="https://github.com/user-attachments/assets/b3f63fd8-dde7-4725-b1f6-1c8036b58683" />


In one terminal

Step 1: List files in the home directory

ls

suconnect

Step 2: Read the current level password

cat /etc/bandit_pass/bandit20

XXXXXXXXXXXX

In another termianl,

Step 3:Start a TCP listener using netcat

Open Terminal 1 and start listening on port 2222.

nc -lvp 2222

Output:

Listening on 0.0.0.0 2222

Terminal 2 (Client)

Step 4: Run suconnect with the listening port

Open Terminal 2 and execute the suconnect binary.

./suconnect 2222

Step 5: Observe password verification

Output in Terminal 2:

Read: XXXXXXXXXXX

Password matches, sending next password

Back to Terminal 1

Step 7: Receive the next password

Output in Terminal 1:

Connection received on localhost

XXXXXXXXXXXXX

YYYYYYYYYYYYY

Output should look something like this:

<img width="1562" height="367" alt="image" src="https://github.com/user-attachments/assets/37548b42-caa7-4c06-893b-4dd829350b39" />

<img width="963" height="248" alt="image" src="https://github.com/user-attachments/assets/8b6f9ca8-c31b-448c-8419-a46d2f64f0ca" />

