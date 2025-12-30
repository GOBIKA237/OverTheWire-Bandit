Level Goal

The password for the next level is stored in the file data.txt next to the word millionth

Use the password we got earlier and using ssh try to connect to host with bandit7 user

<img width="1525" height="215" alt="image" src="https://github.com/user-attachments/assets/11b05895-4240-40f5-bf17-df90a95e3b00" />

Step 1: Use the ls command to see the available files.

ls

data.txt

Step 2: Count the number of lines to understand the file size.

wc -l data.txt

98567 data.txt

Step 3: The password is located on the line containing the word “millionth”.
Use grep to search for that keyword.

cat data.txt | grep "millionth"

Output should look something like this:

<img width="1059" height="338" alt="image" src="https://github.com/user-attachments/assets/1e451829-6c55-417f-925e-87df84a6b471" />




