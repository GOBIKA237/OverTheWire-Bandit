Level Goal

There is a git repository at ssh://bandit29-git@bandit.labs.overthewire.org/home/bandit29-git/repo via the port 2220. The password for the user bandit29-git is the same as for the user bandit29.

1.Create a directory and move into it

mkdir ~/bandit29-repo

cd ~/bandit29-repo

2.Clone the Bandit Level 29 Git repository

git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo

Enter the Bandit29 password when prompted.

3.Enter the cloned repository

cd repo

4.List repository contents

ls

README.md is present.

5.Read the README file

cat README.md

The password is not shown (<no passwords in production!>).

6.Check commit history

git log

Commits such as:fix username,initial commit of README.md

No password is revealed here.

List all remote branches

7.git branch -r

Available branches:

origin/master

origin/dev

origin/sploits-dev

8.Switch to the dev branch

git checkout dev

A new local branch dev is created tracking origin/dev

9.List files in the dev branch

ls

A new directory code appears along with README.md.

10.Read the README file again

cat README.md

11.Obtain Level 30 credentials

Username: bandit30

Password:<bandit29 pass>

SCREENSHOTS

<img width="598" height="530" alt="image" src="https://github.com/user-attachments/assets/f0a94510-134f-46c2-9cab-c597d274d7a1" />

<img width="846" height="613" alt="image" src="https://github.com/user-attachments/assets/453abd24-341a-428d-9f7b-3c00f8258c19" />

<img width="595" height="488" alt="image" src="https://github.com/user-attachments/assets/66f969d4-1604-4b04-8a52-fd8d38518db8" />


