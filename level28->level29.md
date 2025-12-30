Level Goal

There is a git repository at ssh://bandit28-git@bandit.labs.overthewire.org/home/bandit28-git/repo via the port 2220. The password for the user bandit28-git is the same as for the user bandit28.

Steps:
1.Create a directory and move into it

mkdir ~/bandit28-repo

cd ~/bandit28-repo

2.Clone the Bandit Level 28 Git repository

git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo

Enter the Bandit28 password when prompted.

3.Enter the cloned repository

cd repo

4.List files in the repository

ls

A README.md file is present.

5.View the README file

cat README.md

The password is hidden (shown as xxxxxxxxxx).

6.Check the commit history

git log

7.Checkout the previous commit where data was added

git checkout 8b7c651b37ce7a94633b7b7c980ded19a16e4f

8.Read the README file again

cat README.md

9.Obtain Level 29 credentials

Username: bandit29

Password:<bandit_29 pass>

SCREENSHOTS:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a7c484aa-481a-477e-be24-5868e6bc4e60" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/51df072c-2a5a-432f-8332-debadc5ac93a" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d25c503a-dc8d-4605-8d7b-691aa88b3353" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/aa45903a-d996-4005-8eca-94cf26ac0a8f" />


