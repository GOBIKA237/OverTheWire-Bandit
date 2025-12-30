Level Goal

There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

Step 1: List files in the home directory

ls

passwords.new  passwords.old

Step 2: Compare the two files

Use the diff command to find differences between the files.

diff passwords.new passwords.old

Step 3: Analyze the output

The new password is the line marked with <.

Step 4: Identify the password for bandit18

Step 5: Exit the session

exit

<img width="738" height="328" alt="image" src="https://github.com/user-attachments/assets/15ab4d87-0326-4289-9809-023d7a0638a6" />

Step 6: Login to Bandit Level 18

Use the retrieved password to login.

ssh bandit18@bandit.labs.overthewire.org -p 2220

<img width="1560" height="603" alt="image" src="https://github.com/user-attachments/assets/f9caab72-d66f-433e-b172-4649d33253ce" />

<img width="1478" height="607" alt="image" src="https://github.com/user-attachments/assets/51e777a0-4b82-4bf8-af5a-b0d5d7e5b710" />

