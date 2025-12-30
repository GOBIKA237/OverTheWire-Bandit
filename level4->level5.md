Level Goal

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

Try connecting to bandit4 using ssh command and the password we got from earlier

<img width="1551" height="637" alt="image" src="https://github.com/user-attachments/assets/e0a12ffc-4888-4fb2-b232-4c7582f6e04c" />

Use the ls command to identify available directories.

ls

inhere

Use the cd command to move into the inhere directory.

cd inhere

Use ls -la to view all files in the directory.

ls -la

-file00  -file01  -file02  -file03  -file04
-file05  -file06  -file07  -file08  -file09

Check the file types to find the human-readable (ASCII text) file.

file ./-file0*

./-file07: ASCII text

Use the cat command to read the file.

cat ./-file07

Output should look like this

<img width="1158" height="778" alt="image" src="https://github.com/user-attachments/assets/c6d960ea-b193-4792-89cb-2767193017ff" />
