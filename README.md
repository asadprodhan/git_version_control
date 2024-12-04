# **How to Use Git Version Control** <br />

### **AUTHOR: Dr Asad Prodhan** https://asadprodhan.github.io/

<br />


## Windows Users

## **Step 1: What does data visualisation do?**

# Checking existing ssh key
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys 

git config --global user.name "Asad Prodhan"
git config --global user.email "prodhan82@email.com"

# Generated SSH key for GitHub

# The codes to generate a ssh key:

ssh -T git@github.com
git config --global user.name "Asad Prodhan"
git config --global user.email "prodhan82@email.com"
ssh -T git@github.com
git --version
ssh -T git@github.com
ls .ssh
eval `ssh-agent`
ssh-keygen
ssh-add /root/.ssh/id_rsa
cat /root/.ssh/id_rsa.pub



ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQD7RZbaHEEwCjdoIH4CXTY96532qJBBd4WaWBcMny4GP0DlDEIT3FAK13yR8eyhcHkqpRVb4xjbm7sbpeZwJPJ3gpidWtJNHmnZ2+uhPInObV3gN+ehElU+696JilacWve9yl7ctEtLUTot8IG6VF0KvqGuWtos3svIHQcLf2zM63bePgWAB2hvvQj6DJXumalER5BC9XuNu9vvPzwGfUCiFSXAT7MOJ7gWe1092ncl5phlxhFiCePPtxh/bRzU4jXhNsz9nokvVXcnmMvkTm7Bh6Cn9ufiXibCr94ZrggXERJataxw5JfJjZ/6GP008Hq5OIa4z90xkObhn1xf0RC/ root@rna-seq

Paste this key to the GitHub new shh key section and authenticate


# Let's create a git repo

mkdir gitgood
cd gitgood

# Let's initiate the repo
git init
If it works, you see the following mesage
Initialized empty Git repository in /data/workshop_git/gitgood/.git/

Once we have run git init on a directory, there is no need to run it again in subdirectories of the original directory. That’s why we should run the command on the parent directory of the project, and we can include additional subdirectories as needed.

git init initializes a repository.
Git stores all of its repository data in the .git directory.

# This doesn't show anything
ls

# This shows the following
ls -a
. .. .git 
. is the current directory
.. one directory before

# We can now try one of the most important Git commands, which tells us the current state of our repository:
git status
Output:
On branch master
No commits yet
nothing to commit (create/copy files and use "git add" to track)

# Let's create documents within the repo
touch README.md

nano README.md

Or
Open the folder in VS Code and then open the README.md file and write

git add README.md

git commit -m "first commit"

git branch
master

git branch -M main
master renamed to main

Create a repo in GitHub but don't include a README.md file in there

git remote set-url origin https://github.com/asadprodhan/git_version_control.git
Authenticate
git remote -v
git push -u origin main

Keep writing the README.md file in VSCode
and 
git add README.md

git commit -m "message"
git push -u origin main

