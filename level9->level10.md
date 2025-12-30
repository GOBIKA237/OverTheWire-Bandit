Level Goal

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

Use ssh command to connect to bandit9 with the password we got earlier

<img width="1526" height="499" alt="image" src="https://github.com/user-attachments/assets/4dc86deb-c32d-40f8-9dd0-35d218545d1f" />

Step 1:Use the ls command to identify the available file.

ls

data.txt

Step 2: The file contains non-printable characters. Use the strings command to extract human-readable text and filter lines containing the = character.

strings data.txt | grep =

Step 3: Identify the password as mentioned with several "=" before it.

<img width="790" height="590" alt="image" src="https://github.com/user-attachments/assets/b35a5f6a-78ba-40ba-a85a-3828c854f5dc" />

