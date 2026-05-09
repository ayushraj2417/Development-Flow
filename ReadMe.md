Developer Onboarding Checklist:
- Environment: AVD (Christies Local Environment) 
- Installation & Access: VS Code, Git CLI, AZ CLI, repo clone, PIM roles. 
- Workflow: Modify → Validate → PR → Merge → Deploy. 

-----------------------------------------------------------------------------
Git & Branching Strategy and workflow:  
1. Please confirm the repository name and branch that contains the latest code or configuration for working on the task of creating an Azure Function App 

2. When you have the above details, clone the repo to your local (AVD) 
Open the git cli and run below command to start development 
Command: git clone repo_url 

3. Open the directory 
Command : cd repo_folder  

4. Open vscode 
Command: code .   (shortcut)  

5. Check out to the latest branch 
Command: git checkout latest_branch (as per the input received mentioned in pointer 1) 

6. Create a development branch as per below branch naming convention 
Command: git checkout –b DO-1143-dataverse 
- Branch naming: DO-<TicketNumber>-<Feature> 

7. Make the changes wrt to your feature or task and validate/plan the changes with the bicep command locally. Once you find code is able to plan successfully then push the changes to git remote (github) with the below Commands.   

Git Push Commands: 
git add .    #Add all modified files 
git add <filename>   # Add a specific file 
git commit –m “Commit message” (Example of commit message: "changes made for new function app" ) 
git push origin branch-name (branch-name: Your branch name) 


8. Create Pull Request 
Go to your Git platform and find your repository 
Source branch: Your feature branch. 
Target branch: main or development. 
Add title, description, and link work items if needed. 
Assign approvers:  
Russell (n0fixedab0de) 
James (MrJGrav) 
Kuba (d-kuba) 
Chris (c10gue) 
Devo 
 
- PR workflow: Create branch → Commit → PR → Review → Merge. 
- Merge strategy: Squash merger preferred for clean history. (Advised by Russel) 

---------------------------------------------------------------------------------------------------------
Some useful Git Commands:  
git status (Show the working directory status) 
git branch (List local branches) 
git branch –a (List all branches (local + remote) 
git branch <branch-name> (Create a new branch) 
git checkout <branch-name> (Switch to a branch) 
git merge <branch-name> – Merge a branch into the current branch 

Git Merge and Merge Conflict:  https://www.geeksforgeeks.org/git/git-merge/ 

A merge conflict occurs when: 
Two branches modify the same part of a file differently. 
Git cannot automatically decide which change to keep. 


How to resolve merge conflicts:  
First, talk to the user who made changes to the same file and understand which changes should be proceeded with.  

There are multiples ways to resolve merge conflicts. Below are the two approaches-- 
git pull  
Then check status: git status  
You will see like: Unmerged paths: both modified: <file> 
Open the files having conflicts and accept Incoming changes or Your changes as per discussion with the user who made changes in the file. 

git fetch  
Command: git fetch origin
git merge origin/<branch-name>
