# **How to Use Git Version Control** <br />

### **AUTHOR: Dr Asad Prodhan** https://asadprodhan.github.io/

<br />


## What is Git Version Control


Git Version Control is a system that can track changes in a document. Like the track change option in a microsoft word document. However, the Git Version Control and the Microsoft Track Change are different in their scopes, functionality, and purposes. See the comparision below:


| **Aspect**              | **Git Version Control**                                                                                      | **Microsoft Word Track Changes**                                                                |
|--------------------------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **Purpose and Scope**    | Tracks changes in code and project files across an entire repository.                                        | Tracks changes in a single text document (e.g., edits, comments, formatting).                  |
| **Granularity**          | Tracks changes at the **line-level** across multiple files.                                                 | Tracks changes at the **character or word-level** in a single document.                        |
| **Collaboration**        | Supports distributed collaboration with each user having a local copy of the repository.                    | Centralized editing; changes are visible within the shared document or during real-time edits. |
| **Version History**      | Maintains a detailed history of all commits and allows reversion to any previous state.                     | Limited versioning tied to the document; relies on manual saves or cloud services for history. |
| **File Types**           | Works with any file type, especially text-based files like code or configuration files.                     | Limited to `.docx` or compatible Word formats.                                                 |
| **Conflict Resolution**  | Resolves merge conflicts programmatically or manually during file merges.                                   | Highlights conflicts inline for manual resolution by users.                                    |
| **Branching and Merging**| Supports branching for parallel development and merging for integration of changes.                        | Does not support branching; all edits are applied directly to the document.                   |
| **Offline Usage**        | Fully functional offline; all repositories are local copies.                                                | Requires the document and Track Changes settings to be available locally.                     |
| **Primary Use Case**     | Best for software development, managing large codebases, and collaborative coding projects.                 | Best for collaborative text document editing, such as writing and reviewing reports.           |



## **How to use the Git Version Control**



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



ssh-rsa XXXXX

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

