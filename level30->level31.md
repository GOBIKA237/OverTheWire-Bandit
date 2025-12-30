Level Goal

There is a git repository at ssh://bandit30-git@bandit.labs.overthewire.org/home/bandit30-git/repo via the port 2220. The password for the user bandit30-git is the same as for the user bandit30.

Clone the repository and find the password for the next level.

1.Create a directory and move into it

mkdir ~/bandit30-repo

cd ~/bandit30-repo

2.Clone the Bandit Level 30 Git repository

git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo

Enter the Bandit30 password when prompted.

3.Enter the cloned repository

cd repo

4.List repository files

ls

Only README.md is present.

5.Read the README file

cat README.md

The file contains no useful information.

6.Check commit history

git log

Only an initial commit exists.

7.List remote branches

git branch -r

Only origin/master is available.

8.List Git tags

git tag

A tag named secret is found.

9.View the contents of the secret tag

git show secret

the password shows

SCREENSHOTS

<img width="921" height="494" alt="image" src="https://github.com/user-attachments/assets/a6bf8697-c7e6-4a0e-afb8-29d074b2730b" />

<img width="843" height="456" alt="image" src="https://github.com/user-attachments/assets/38c3e38f-b291-4f17-a9d5-fefbd23013cf" />

<img width="553" height="254" alt="image" src="https://github.com/user-attachments/assets/76ca477a-c0b5-41b3-8ef0-990ae0af3cc8" />
