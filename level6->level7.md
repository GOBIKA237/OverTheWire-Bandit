Level Goal

The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size

Use the password we got earlier to connect to bandit6 using ssh command

<img width="1595" height="499" alt="image" src="https://github.com/user-attachments/assets/b587eb37-841d-44c9-bb91-eeee700867c1" />

Step 1:Use the ls command to view the current directory.

ls

Step 2: Search for the required file

The password is stored in a file that meets the following conditions: Regular file,Owned by user bandit7,Belongs to group bandit6 and File size is 33 bytes

Search the entire filesystem and suppress permission errors:

find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null

Step 3: Identify the password file

/var/lib/dpkg/info/bandit7.password

Step 4: Use the cat command to read the password.

cat /var/lib/dpkg/info/bandit7.password

<img width="1525" height="215" alt="image" src="https://github.com/user-attachments/assets/e5c3cec1-7b10-4937-b32a-79f47974c3ee" />
