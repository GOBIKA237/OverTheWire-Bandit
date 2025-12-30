Level Goal

There is a git repository at ssh://bandit27-git@bandit.labs.overthewire.org/home/bandit27-git/repo via the port 2220. The password for the user bandit27-git is the same as for the user bandit27.

Clone the repository and find the password for the next level.

Before executing make sure you are in local machine path.

1. Create a directory

mkdir ~/bandit27-repo

cd ~/bandit27-repo

2. Clone the Git repository

git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo

Enter bandit27 password when prompted

3. Enter the cloned repository

cd repo

4. List files

ls

README

5. Read the README file

cat README

6. Get the password

The README displays:

The password to the next level is: bandit28_password

SCREENSHOTS:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b0841d3c-8f8c-41db-85a4-e252c66755da" />

<img width="1099" height="444" alt="image" src="https://github.com/user-attachments/assets/4b969fb8-133f-47e4-a36b-fefd19d7019d" />


