Level Goal

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

Use ssh command and the password we got earlier to connect to host as bandit12

<img width="1453" height="524" alt="image" src="https://github.com/user-attachments/assets/91a9765e-c64b-4934-83bd-918e4d74bb7d" />

Step 1: List files in the home directory

ls

data.txt

Step 2: Create a writable directory

Home directory is read-only, so move to /tmp.

cd /tmp

mkdir gobika12345

Step 3: Copy the file to /tmp

cp ~/data.txt /tmp/gobika12345

Step 4: Move into the working directory

cd /tmp/gobika12345

Step 5: Convert hex dump back to binary

cat data.txt | xxd -r > hexdump

Step 6: Identify the file type

file hexdump

Output: gzip compressed data

Step 7: Rename and decompress (gzip)

mv hexdump hexdump.gz

gzip -d hexdump.gz

Step 8: Check file type again

file hexdump

Output: bzip2 compressed data

Step 9: Rename and decompress (bzip2)

mv hexdump hexdump.bz2

bzip2 -d hexdump.bz2

Step 10: Check file type again

file hexdump

Output: gzip compressed data

Step 11: Rename and decompress (gzip)

mv hexdump hexdump.gz

gzip -d hexdump.gz

Step 12: Identify tar archive

file hexdump

Output: POSIX tar archive

Step 13: Extract tar file

tar -xvf hexdump

Step 14: Repeat extraction steps

Keep repeating file → rename → decompress/extract until you reach a readable ASCII file.

Final readable file:

file data8.bin

Step 15: View the password

cat data8.bin

This task is just renaming and extracting files until we reach the human readable content.

<img width="802" height="616" alt="image" src="https://github.com/user-attachments/assets/2c46a3af-30d9-4ece-aeed-ad4f8245e8a5" />

<img width="1264" height="703" alt="image" src="https://github.com/user-attachments/assets/71f4a3bd-c406-488e-b1dd-90519adb07ce" />

<img width="835" height="763" alt="image" src="https://github.com/user-attachments/assets/3319b527-c8fb-4b9d-b015-248203dd8f3f" />






