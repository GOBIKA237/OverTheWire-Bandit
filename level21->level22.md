Level Goal

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

Step 1: Login to Bandit Level 21

<img width="1526" height="660" alt="image" src="https://github.com/user-attachments/assets/3e43e935-3d27-427e-8c2a-a291485b7857" />

Step 2: List files in the home directory

ls

Step 3: Navigate to cron jobs directory

cd /etc/cron.d

Step 4: List all cron job files

ls -la

cronjob_bandit22(what we need)

Step 5: Read the cron job for bandit22

cat cronjob_bandit22

@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null

Step 6: Read the cron job script

cat /usr/bin/cronjob_bandit22.sh

Step 7: Understand what the script does

#!/bin/bash

chmod 644 /tmp/t706lds9S0RqQh9aMcz6ShpAoZKF7fgv

cat /etc/bandit_pass/bandit22 > /tmp/t706lds9S0RqQh9aMcz6ShpAoZKF7fgv

Copies bandit22 password

Stores it in a world-readable file in /tmp

Step 8: Read the generated file in /tmp

cat /tmp/t706lds9S0RqQh9aMcz6ShpAoZKF7fgv

This shows password for next level.


Output looks like this:

<img width="1356" height="768" alt="image" src="https://github.com/user-attachments/assets/7d1376e5-a105-44cc-a27f-edf986b65402" />

<img width="1370" height="494" alt="image" src="https://github.com/user-attachments/assets/d7fc41c0-1cde-40b0-ad48-5114264d0ef7" />


