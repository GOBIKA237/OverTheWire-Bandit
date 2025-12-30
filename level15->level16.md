Level Goal

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

Use ssh command and the password we gott from eariler and try to log in as user bandit15 to the host

<img width="1013" height="395" alt="image" src="https://github.com/user-attachments/assets/a246c05c-cbee-4608-a842-ab2477ec3900" />

Step 1: Read the current level password
cat /etc/bandit_pass/bandit15

Output:

XXXXXXXXXXXXXXXXXX

Step 2: Understand the service requirement

The next password is obtained by connecting to:Host: localhost,Port: 30001 and Protocol: SSL

Step 3: Connect using correct SSL flag

ncat localhost 30001 --ssl

Step 4: Send the current password

After connecting, paste the password and press Enter.

XXXXXXXXXXXX

Step 5: Receive the next password

Output should look like this:

<img width="1125" height="357" alt="image" src="https://github.com/user-attachments/assets/d4f8881a-4afb-4852-9c07-209a3b55d080" />

