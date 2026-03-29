1) What is Git?
Git is a version control system used to track changes in a project.

=>Why Git is useful
Tracks code history
Helps revert to older versions
Shows what changed and when
Makes collaboration easier
Useful for both personal and team projects
Example:-
If code works today but breaks tomorrow, Git helps restore the earlier working version.

2) What is a Repository?
A repository (repo) is a project folder that Git tracks.
It contains:
source code
files and folders
project history
commits

3) Install and Setup Git
Install Git
Download from: git-scm.com

Configure Git (first-time setup)
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
Why this is needed:
Git uses this information to identify who made each commit.

Git Commands-
1.Initialize a Git Repository
To start tracking a project with Git:
git init :- 
What it does
Initializes Git inside the folder
Creates a hidden .git directory
Starts version control for the project

2. Check Project Status
git status
Purpose
Shows:
new files
modified files
staged files
unstaged files
Use case
This is one of the most commonly used Git commands.

3)Staging Area
The staging area is used to prepare changes before committing them.
Purpose of staging
It allows selective commits.
Why it matters
Not every changed file must be committed immediately.
Example:
one file contains a bug fix
another file contains incomplete work
Only the bug fix can be staged and committed.

4)Add Files to Stage
Add a specific file
git add filename
Example:
git add app.java
Add all files
git add .
Meaning
Moves changes to the staging area so they are ready for commit.

5)Commit Changes
A commit is a saved snapshot of the project.
Command
git commit -m "commit message"
Example
git commit -m "Added login functionality"
Good commit message rules
short
meaningful
describes the actual change
Good examples
Added login API
Fixed null pointer issue
Updated README

6)View Commit History
git log
What it shows
commit hash
author
date
commit message
Purpose
Used to review project history.

7)Remove a File from Stage
If a file was staged by mistake:
git restore --staged filename
Example
git restore --staged app.java
What it does
Removes the file from staging without deleting code changes.

8)Stashing Changes
Stash is used to temporarily save unfinished work without committing it.
Save current changes
git stash
Restore stashed changes
git stash pop
Delete all stash entries
git stash clear
Use case
Useful when:
switching tasks
changing branches
pausing incomplete work

9)Connect Local Project to GitHub
After creating a repository on GitHub, connect it to the local project.
Command
git remote add origin <repository-url>
Example
git remote add origin https://github.com/username/my-project.git
Purpose
Links local repository with remote GitHub repository.

10)Push Code to GitHub
Command
git push -u origin main
(older repos may use master instead of main)
Purpose
Uploads local commits to GitHub.

11)Full Workflow to Send Code to GitHub
git init
git add .
git commit -m "Initial commit"
git remote add origin <repo-url>
git push -u origin main
Meaning
initialize repo
stage files
commit changes
connect to GitHub
push code online

12)Branches
A branch is a separate line of development.
Why branches are useful
They allow work on:
new features
bug fixes
experiments
without affecting the main codebase.

13)Main Branch
The default branch is usually:
main
or in older projects:
master
This is usually the stable version of the project.

14) Create and Switch Branches
Create a branch
git branch feature-login
Switch to a branch
git checkout feature-login
Create and switch in one command
git checkout -b feature-login
Use case
Create a separate workspace for a specific feature or fix.

15) Merge Branches
Merge is used to bring changes from one branch into another.
Command
git merge branch-name
Example
git merge feature-login
Use case
Used after feature development is complete and ready to combine with main.

16) Forking
A fork is a copy of someone else’s GitHub repository into your own GitHub account.
Why it is used
Mainly for:
open-source contribution
external collaboration
Benefit
Allows working on another project without directly changing the original repository.

17) Cloning a Repository
Cloning downloads a GitHub repository to the local machine.
Command
git clone <repo-url>
Example
git clone https://github.com/username/project.git
Purpose
Used to bring a remote project to the local system for development.

18) Upstream Repository
When working with a forked repository, the original repository is usually added as upstream.
Command
git remote add upstream <original-repo-url>
Purpose
Helps keep the fork updated with the original project.

19) Pull Request (PR)
A Pull Request is a request to merge your changes into another branch or repository.
Use case
Common in:
team collaboration
code reviews
open-source contribution
Typical flow
Fork repository
Clone it locally
Create a new branch
Make changes
Commit changes
Push branch
Open Pull Request on GitHub

20) Force Push
Command
git push --force
Use case
Used when commit history has been rewritten (for example after rebase or squash).
Warning
Should be used carefully, especially in shared branches.

21) Squashing Commits
Squashing means combining multiple commits into a single commit.
Why it is useful
Keeps Git history:
cleaner
easier to read
more professional
Example
Instead of:
fixed typo
fixed typo again
small change
Can be squashed into:
Updated README and fixed formatting

22) Rebase
Rebase is used to move or reapply commits on top of another branch.
Why it is useful
Helps maintain a cleaner and more linear Git history.
Common use
Used before merging to avoid unnecessary messy commit history.

23) Merge Conflicts
A merge conflict happens when Git cannot automatically decide which code should stay.
Common reason
Two branches modify the same line or nearby section of code.

24) How to Fix a Merge Conflict
When a conflict happens, Git marks it inside the file like this:
<<<<<<< HEAD
your code
=======
incoming code
>>>>>>> branch-name

=>Steps to resolve:-
1.Open the conflicted file
2.Review both code versions
3.Decide what final code should remain
4.Remove conflict markers
5.Save the file
6.Stage the file
7Commit the resolution
==>Commands:-
git add .
git commit -m "Resolved merge conflict"

25) Important Git Commands Summary
Setup
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git init
Status
git status
Stage and Commit
git add .
git add filename
git commit -m "message"
History
git log
Unstage
git restore --staged filename
Stash
git stash
git stash pop
git stash clear
GitHub
git remote add origin <repo-url>
git push -u origin main
Branching
git branch feature-name
git checkout feature-name
git checkout -b feature-name
Merge
git merge branch-name
Clone / Fork Workflow
git clone <repo-url>
git remote add upstream <repo-url>

26) Quick Answers

How to send code to GitHub?
git init
git add .
git commit -m "Initial commit"
git remote add origin <repo-url>
git push -u origin main

What does the stage area do?
It prepares selected changes for the next commit.

How to fix a merge conflict?
open conflicted file
remove conflict markers
keep correct code
save
stage
commit
===================***************************************************************============================================
