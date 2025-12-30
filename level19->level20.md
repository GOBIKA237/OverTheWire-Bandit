Level Goal

To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

Step 1: List files in the home directory

ls

bandit20-do

Step 2: Identify the purpose of the binary

The file bandit20-do allows executing commands as bandit20.

Step 3: Verify effective user ID

Run the id command using the binary.

./bandit20-do id

uid=11019(bandit19) gid=11019(bandit19) euid=11020(bandit20)

This confirms the binary runs commands with bandit20 privileges.

Step 4: Test the effective user
./bandit20-do whoami

bandit20

Step 5: Use the absolute path to read the password 

./bandit20-do cat /etc/bandit_pass/bandit20

XXXXXXXXXX

Output would look ssomething like this:

<img width="1730" height="413" alt="image" src="https://github.com/user-attachments/assets/67c7161a-24f8-434b-8292-23f8211823a0" />
