Level Goal

Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

Step 1: Login using the provided SSH private key

<img width="1521" height="546" alt="image" src="https://github.com/user-attachments/assets/76903518-3c4b-4f77-bc43-7873a4bc4262" />

Login is successful, but the shell is restricted.

Step 2:Observe the restricted environment

After login:

Commands do not work normally

You are dropped into a limited session

A pager (like less) is used

Step 3:Resize the terminal window

Make the terminal window very small(this forces the pager to stay open)

This is critical to bypass the restricted shell.

Step 4: Trigger help inside the pager

Press:

v

This opens vi editor inside the pager.

Step 5: Escape to a shell from vi

Inside vi, type:

:set shell=/bin/bash. Press Enter

:shell. Press Enter.

normal shell as bandit26 is visible.

Step 6:Read the password file

cat /etc/bandit_pass/bandit26

XXXXXXXXXXX(password for next level)

SCREENSHOTS:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d6a3594c-2145-4602-888b-b1e08dd0b942" />

<img width="1089" height="392" alt="image" src="https://github.com/user-attachments/assets/385e35f1-a120-4558-ace2-4fe250d6cb30" />
