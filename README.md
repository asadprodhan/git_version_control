<h1 align="center">How to Use Git Version Control</h1>


<h3 align="center">M. Asaduzzaman Prodhan<sup>*</sup></h3>


<div align="center"><b> School of Biological Sciences, The University of Western Australia </b></div>


<div align="center"><b> 35 Stirling Highway, Perth, WA 6009, Australia. <sup>*</sup>Correspondence: prodhan82@gmail.com </b></div>


<br />


<p align="center">
  <a href="https://github.com/asadprodhan/git_version_control/tree/main#GPL-3.0-1-ov-file"><img src="https://img.shields.io/badge/License-GPL%203.0-yellow.svg" alt="License GPL 3.0" style="display: inline-block;"></a>
  <a href="https://orcid.org/0000-0002-1320-3486"><img src="https://img.shields.io/badge/ORCID-green?style=flat-square&logo=ORCID&logoColor=white" alt="ORCID" style="display: inline-block;"></a>
</p>


<br />

## What is Git Version Control


Git Version Control is a system that can track changes in a document. Like the track change option in a microsoft word document. However, the Git Version Control and the Microsoft Track Change are different in their scopes, functionality, and purposes. See the comparision below:


<br />


| **Aspect**              | **Git Version Control**                                                                                      | **Microsoft Word Track Changes**                                                                |
|:-------------------------|:------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| **Purpose and Scope**    | Tracks changes in code and project files across an entire repository.                                        | Tracks changes in a single text document (e.g., edits, comments, formatting).                  |
| **Granularity**          | Tracks changes at the **line-level** across multiple files.                                                 | Tracks changes at the **character or word-level** in a single document.                        |
| **Collaboration**        | Supports distributed collaboration with each user having a local copy of the repository.                    | Centralized editing; changes are visible within the shared document or during real-time edits. |
| **Version History**      | Maintains a detailed history of all commits and allows reversion to any previous state.                     | Limited versioning tied to the document; relies on manual saves or cloud services for history. |
| **File Types**           | Works with any file type, especially text-based files like code or configuration files.                     | Limited to `.docx` or compatible Word formats.                                                 |
| **Conflict Resolution**  | Resolves merge conflicts programmatically or manually during file merges.                                   | Highlights conflicts inline for manual resolution by users.                                    |
| **Branching and Merging**| Supports branching for parallel development and merging for integration of changes.                        | Does not support branching; all edits are applied directly to the document.                   |
| **Offline Usage**        | Fully functional offline; all repositories are local copies.                                                | Requires the document and Track Changes settings to be available locally.                     |
| **Primary Use Case**     | Best for software development, managing large codebases, and collaborative coding projects.                 | Best for collaborative text document editing, such as writing and reviewing reports.           |
------------------------------------------------------------------------------------------------


<br />


## **How to use the Git Version Control in Windows computer**


## Requirements

- `Download Visual Studio Code


- Create a GitHub account


- Create a GitHub repository and name it git_version_control (for example) 


## **Open a terminal in Visual Studio Code**

See an example below:


<br />

<p align="center">
  <img 
    src="https://github.com/asadprodhan/git_version_control/blob/main/vs_code_annot.PNG"
 align="center" width=100% height=100% >   
</p>
<p align = center>
Figure 1: Writing a GitHub repository using VS Code.
</p>


## Step 1


- Set GitBash in the terminal


- Create a directory in your local computer


- Initiate a GitHub repository


```
git init
```


```
mkdir git_version_control
```

- Create a README file


```
touch README.md
```


## Step 2


- Open the git_version_control directory that you have created in Step 1


## Step 3


- Open the README.md file by clicking on it


## Step 4


- Start writing your README doc and save by using ctrl-S


## Step 5


- Open a preview panel for your README markdown document


## Step 6

- Collect the URL of your online GitHub repo

- Add the remote URL

```
git remote add origin https://github.com/asadprodhan/git_version_control.git 
```

- Then, verify by running

```
git remote -v
```

You will the URL that you have added above.

- Connect your local GitHub repo (git_version_control) to your online GitHub repo (git_version_control)

```
git remote set-url origin https://github.com/asadprodhan/git_version_control.git
```


## Step 7


- Check the status of your files

```
git status
```

- Stage the changes

```
git add .
```

- Commit the changes with a message

```
git commit -m "message"
```

## Step 8

- Check existing branch

```
git branch
```

If it is "master", then change it to "main"

```
git branch -m master main
```

- Push the changes to your online GitHub repository

```
git push -u origin main
```

## Note

If your push is rejected because the remote repository contains changes that your local repository doesn't have.

Then, pull and push again like as follows


```
git pull --rebase origin main
```


```
git push -u origin main
```


Or, force your push if you're sure that you don't need the remote changes

```
git push -f origin main
```

<br />

# FAQ

## How to upload images from local computer to the GitHub repository?


- Add a specific image


```
git add <image_file_name>
```

- Or add all changes

```
git add .
```

- Stage the changes

```
git commit -m "message"
```


- Push the changes to the online GitHub repository


```
git push -u origin main
```

## How to display the image in README document 


- Collect the image path from your GitHub repository by righ-clicking on the image and copying the link


- Add the following add chunk to your README document


<br />

```
<p align="center">
  <img 
    src="https://github.com/asadprodhan/git_version_control/blob/main/vs_code_annot.PNG"
 align="center" width=100% height=100% >   
</p>
<p align = center>
Figure 1: Blastn database nt files.
</p>
```


The above code produces the following display.


<br />

<p align="center">
  <img 
    src="https://github.com/asadprodhan/git_version_control/blob/main/vs_code_annot.PNG"
 align="center" width=100% height=100% >   
</p>
<p align = center>
Figure 1: Writing a GitHub repository using VS Code.
</p>
