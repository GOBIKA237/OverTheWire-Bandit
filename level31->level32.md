Level Goal

There is a git repository at ssh://bandit31-git@bandit.labs.overthewire.org/home/bandit31-git/repo via the port 2220. The password for the user bandit31-git is the same as for the user bandit31.

Clone the repository and find the password for the next level.

1. Create a working directory

mkdir ~/bandit31-repo

cd ~/bandit31-repo

2. Clone the Bandit Level 31 repository

git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo

Enter the Bandit31 password when prompted.

3.Move into the repository

cd repo

4.List repository contents

ls

README.md is present.

5. Read the README file

cat README.md

File name: key.txt

Content: May I come in?

Branch: master

6.Create the required file

echo "May I come in?" > key.txt

Verify the content:

cat key.txt

7. Add the file to Git

git add -f key.txt

8. Configure Git username and email (if not already set)

git config --global user.email "you@example.com"

git config --global user.name "Your Name"

9. Commit the changes

git commit -m "Added key.txt"

10. Push to the remote master branch

git push origin master

11. Obtain the password for the next level

After pushing, the server validates the file and displays the password

SCREENSHOTS:

<img width="834" height="576" alt="image" src="https://github.com/user-attachments/assets/fa802f65-8bcc-42ce-837c-841deb9e5067" />

<img width="667" height="450" alt="image" src="https://github.com/user-attachments/assets/e80e96a9-f926-4bcc-bbc7-d9ff8c846ce6" />

<img width="572" height="300" alt="image" src="https://github.com/user-attachments/assets/9df0ea0d-21b2-4827-baeb-88206b358bd1" />

<img width="689" height="700" alt="image" src="https://github.com/user-attachments/assets/310b9072-7438-42f7-92fb-c065fd22f41e" />

<img width="1082" height="631" alt="image" src="https://github.com/user-attachments/assets/535da7fc-6307-4e66-9bdf-cd0ae4a29d19" />




