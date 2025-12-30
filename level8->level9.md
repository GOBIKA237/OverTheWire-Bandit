Level Goal

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

Use the passoword we got from earlier and try to connect to bandit8 using ssh command

<img width="1293" height="506" alt="image" src="https://github.com/user-attachments/assets/cbddd20f-87bb-46da-b938-d058b4b5dff9" />

Step 1: Use the ls command to identify available files.

ls

data.txt

Step 2: The password is stored in the line that appears only once in the file.
To find it, sort the file and count repeated lines using uniq -c.

cat data.txt | sort | uniq -c

Step 3: Look for the line with a count of 1, which indicates it appears only once.

Output should look something like this:

<img width="965" height="584" alt="image" src="https://github.com/user-attachments/assets/baef931f-7811-4762-abf3-5f7c5a3b358a" />
