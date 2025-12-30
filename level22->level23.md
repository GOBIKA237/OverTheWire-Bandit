Level Goal

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

Step 1: Login to Bandit Level 22
ssh bandit22@bandit.labs.overthewire.org -p 2220
Use ssh command and the password we got earlier and login as user bandit22

<img width="1450" height="577" alt="image" src="https://github.com/user-attachments/assets/8adabc77-808e-4233-a0c3-b986c1d793f4" />

Step 2: List files in the home directory

ls

Step 3: Navigate to the cron jobs directory

cd /etc/cron.d

Step 4: List available cron jobs

ls

Important file found:

cronjob_bandit23

Step 5: Read the cron job configuration

cat cronjob_bandit23

Output:

@reboot bandit23 /usr/bin/cronjob_bandit23.sh &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh &> /dev/null

Step 6: Read the cron job script

cat /usr/bin/cronjob_bandit23.sh

Step 7: Understand the script logic

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
cat /etc/bandit_pass/$myname > /tmp/$mytarget

Uses whoami → bandit23
Generates an MD5 hash from the string
I am user bandit23

Stores the password in /tmp/<md5_hash>

Step 8: Manually calculate the MD5 hash

echo I am user bandit23 | md5sum | cut -d ' ' -f 1

8ca319486bfbbc3663ea0fbe81326349

Step 9:Read the generated password file

cat /tmp/8ca319486bfbbc3663ea0fbe81326349

Returns password for next level

<img width="1585" height="659" alt="image" src="https://github.com/user-attachments/assets/a301fd1a-17c7-45cb-8a8a-088cdb4d4f28" />

<img width="1524" height="265" alt="image" src="https://github.com/user-attachments/assets/5c86ad85-1f07-48e7-b1fc-82bc15ad4da3" />


