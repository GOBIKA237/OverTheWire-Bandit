Level Goal

After all this git stuff, it’s time for another escape. Good luck!

aim:Escape the restricted UPPERCASE shell to execute normal Linux commands and retrieve the password for the next level.

1.Connect to Bandit Level 32

ssh bandit32@bandit.labs.overthewire.org -p 2220

Enter the Bandit32 password when prompted.(we got from previous level)

2. Observe the restricted shell

After login, the system displays:

WELCOME TO THE UPPERCASE SHELL

This shell converts all typed commands to uppercase, preventing normal command execution.

3. Spawn a new shell using $0

$0

$0 launches a new shell instance.

4. Set Bash as the active shell

export SHELL=/bin/bash

Verify:

echo $SHELL

/bin/bash

5. Start the Bash shell

$SHELL

You now have a normal Bash prompt.

6. Read the password file

cat /etc/bandit_pass/bandit33

7. Obtain the password and click exit the terminal or type exit.

SCREENSHOTS:

<img width="877" height="292" alt="image" src="https://github.com/user-attachments/assets/dff93c23-aa20-4e83-8cc6-68d878a047ef" />

<img width="477" height="211" alt="image" src="https://github.com/user-attachments/assets/4388ff48-054a-421d-a5d4-c9d7478f52f4" />

