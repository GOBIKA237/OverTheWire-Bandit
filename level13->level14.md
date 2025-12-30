Level Goal

The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.

Use ssh and the password we got earlier to connect to host with user bandit13

<img width="1074" height="789" alt="image" src="https://github.com/user-attachments/assets/35ebd75e-0dbd-452a-bacc-3688c97c600f" />

Step 1: List files in the home directory
ls

Step 2: List all files including hidden files
ls -la

Step 3: Locate the password file. The password for the next level is stored in the system directory:

/etc/bandit_pass/

Step 4: Read the password file

cat /etc/bandit_pass/bandit14

Output should look something like this:

<img width="668" height="306" alt="image" src="https://github.com/user-attachments/assets/7efc81ef-21a2-4fa2-89f7-b752f02ee935" />







