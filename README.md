# Git and GitHub Command Line Tutorial for a Python course 

### 1. Introduction to Git and GitHub
____  

**What is Git?**  
Git is a version control system that allows you to track changes in your files and collaborate with others.  

**What is GitHub?**   
GitHub is a cloud-based hosting service that lets you manage Git repositories, collaborate on code, and use features like issue tracking, pull requests, and more.

____  

### 2.1. Setting Up GitHub   

Create an account on GitHub   

**Create tokens for repository access**  
https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens   

**Store github token in git**   
https://stackoverflow.com/questions/35942754/how-can-i-save-username-and-password-in-git   

### 2.2. Setting Up git 
Installing Git:

**For Windows :house::**   
Download from [git-scm.com](git-scm.com) and run the installer.  

**For macOS :green_apple::**   
Use Homebrew with the command:  
```
brew install git
```  

**For Linux :penguin::**   
Install via your package manager, e.g., for Debian/Ubuntu:  
```
sudo apt-get install git
```   

**Configuring Git:**  
Set your username and email, which will be associated with your commits:  
``` 
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --list
```

### 3. Creating a Repository on GitHub

1. Go to GitHub and log in.
2. Click on the "New" icon at the top-right corner to create a new repository.
3. Name your repository and make it either public or private.
4. Click on <> Code in the top-right corner to copy the https link for cloning

#### In the terminal
Navigate to the directory where you want your project to be in the terminal:  
```
cd /path/to/your/project
```  

**Clone your repository to directory**

```
git clone https://github.com/vilmacanfjorden/github_tutorial.git
```

![image](https://github.com/user-attachments/assets/971e3aa6-5417-4a79-b2f3-5fd877940ea7)

____  

Make sure you got the repository and `cd` into it

```
ls -l
cd test_repo
```

### 4. Making Your First Commit

Add a file to your repository:  
```
echo "print('Hello World')" > test.py
git status  
```
when using `git status`  it should look something like this:   
![image](https://github.com/user-attachments/assets/1597f6d7-5497-413f-8f10-0865bd197a90)

Add changes to the staging area:  
```
git add test.py
git status
```
After `git add`   
![image](https://github.com/user-attachments/assets/16b41fc4-3701-4012-b120-fe2041425ba8)

Commit the changes:  
``` 
git commit -m "Initial commit"
git status
```
After `git commit`:    
![image](https://github.com/user-attachments/assets/edeaec7f-e0f3-4f8a-8b7a-210478e157bc)


### 5. Push to GitHub  

Push you updates to your repository on GitHub

```
git push
```

### 6. Pull from GitHub  

Go to your repository on github.com
Go to your README.md and edit, write something informative on how to use your code for example:

![image](https://github.com/user-attachments/assets/d18dcd9c-9748-446c-87a0-68441be89f7a)   

Commit the changes by clicking on Commit changes in the top-right corner    
![image](https://github.com/user-attachments/assets/f431fdcc-5753-4841-bcbf-a8456989d4f2)   

Go to your teminal again and make sure you are in the repository and pull the latest changes:

```
git pull
git status
``` 

Now you should have the latest README updated locally as well.


### Conclusion and Best Practices

* Commit Often: Keep commits small and focused.   
* Use Descriptive Commit Messages: Clearly explain what changes were made and why.   
* Pull Before You Push: Always pull the latest changes before pushing to avoid conflicts.
  
* Official Git Documentation: (https://git-scm.com/doc)  
* GitHub Learning Lab: (https://docs.github.com/en/get-started/start-your-journey/git-and-github-learning-resources)  

____   
### Additional information (if you want)
<details>
  <summary>Click to expand!</summary>

### Working with Branches

Create a New Branch:
```
git branch new-feature
```

Switch to the New Branch:
```
git checkout new-feature
```

Switch back to the main branch:
```
git checkout main
```

Merge the branch:
```
git merge new-feature
```

### Handling Common Scenarios

Undo a Commit:
```
git revert <commit_hash>
```

Remove a File from the Staging Area:
```
git reset HEAD <file>
```




