Level Goal

The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

Step 1: Attempt normal SSH login

Normal login immediately logs out, so direct interaction is not possible.

ssh bandit18@bandit.labs.overthewire.org -p 2220

Step 2: Execute a command directly over SSH

Run ls remotely during SSH login.

ssh bandit18@bandit.labs.overthewire.org -p 2220 ls

Step 3: Read the readme file remotely

Use SSH to execute cat readme.

ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme

Step 4: Identify the password from output

Output:

bandit18@bandit.labs.overthewire.org's password:
XXXXXXXXXXXXX

<img width="1361" height="634" alt="image" src="https://github.com/user-attachments/assets/45986741-b4c6-43cd-a1f5-2e40b7ef3daf" />


<img width="1458" height="616" alt="image" src="https://github.com/user-attachments/assets/f694ba9b-9f4f-448b-aed4-57065c457401" />

Try logging in with those credentials:

<img width="1382" height="629" alt="image" src="https://github.com/user-attachments/assets/61c10837-6856-440a-a2fa-134ad69c52cb" />
