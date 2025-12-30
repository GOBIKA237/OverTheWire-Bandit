Level Goal

A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
You do not need to create new connections each time

Step 1: Login to Bandit Level 24

ssh bandit24@bandit.labs.overthewire.org -p 2220

<img width="1504" height="622" alt="image" src="https://github.com/user-attachments/assets/b2daf43f-57ad-4b21-aa15-eaa281b3e54f" />

Step 2:Navigate to the working directory

cd /tmp/gobika1234

Step 3: List files

ls

shell.sh

Step 4: Give execute permission to the script

chmod 777 shell.sh

Step 5: Run the script

./shell.sh

Step 6: Understand the program output

The program says:

I am the pincode checker for user bandit25.
Please enter the password for user bandit24 and the secret pincode
on a single line, separated by a space.

checks:

Current password (bandit24)

4-digit PIN (0000–9999)

Step 7: Script logic

Tries all PINs from 0000 to 9999

Uses the correct bandit24 password

Stops when the program prints Correct!

Step 8: Wait for successful match

After several attempts, the program responds:

Correct!

The password of user bandit25 is XXXXXXXXXXXXXX

SCREENSHOTS:

<img width="1913" height="759" alt="image" src="https://github.com/user-attachments/assets/1aef66ce-7b7d-476e-83a7-292175434495" />

<img width="1683" height="295" alt="image" src="https://github.com/user-attachments/assets/5dc2c7f3-a948-4a08-a23d-ec66684891e8" />


