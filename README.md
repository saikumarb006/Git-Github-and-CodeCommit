# Section-5-Git-Github-and-CodeCommit

# Create local git repository - Lab

**Step 1. Open Terminal in Visual Studio Code**

**Step 2. Now Goto specified location to initialize git**

**Step 3. Type the following commands in VS Code**
```sh
$ cd Documents/Course-Material/
$ mkdir git-demo
# Go to Computer location and check the git-demo folder
$ git status
# It is not a git repository
$ git init
$ touch .gitignore
# Open .gitignore and write ".DS_Store"
$ git status
$ git add .
$ git add .gitignore
$ git status
$ git commit -m "first commit"
$ clear
$ ls -a
$ cd .git
$ ls -a
$ cat config
$ cd ..
$ git config --local user.name "Amit"
$ git config --local user.email teacheramit@gmail.com
$ cat .git/config
$ git config --list
$ git config --global --list
$ rm -rf .git*
```

# error 403 solution:"The requested URL returned error: 403 Forbidden"
```sh
The error may be, the computer has saved a git username and password so if you shift to another account the error 403 will appear.
Below is the solution-
- For Windows 
   - control panel > user accounts > credential manager > Windows credentials > Generic credentials
   - Next, remove the Github keys.
- In mac
  - In Finder, search for the Keychain Access app.
  - In Keychain Access, search for github.com.
  - Find the "internet password" entry for github.com.
  - Edit or delete the entry accordingly.
```


### End of lab


# Create remote Git repository - Lab

**Step 1.Goto www.github.com**

**Step 2. Click on Sign Up**
- Provide user and password 
- Select role 
- Experience
- Plan to use 
- Complete setup
- Click verify email address

**Step 3. Goto your email inbox and verify github account**

**Step 4. Click on "+" sign and click on New repository**

**Step 5. Give name of repository and select Public**
- Click on Create repository
 
**Step 6.Open Terminal in Visual Studio Code**
```sh
$ git init
$ touch .gitignore
# Open .gitignore and write ".DS_Store"
$ git remote add origin https://github.com/teacheramitk/git-demo.git
$ cat .git/config
# Open the keychain in PC and delete the git entry
$ git push -u origin master
# Error due to untracked files
$ git status
$ git add .
$ git commit -m "first commit"
$ git push -u origin main
$ cat .git/config
$ git push -u origin master
# Provide user name and password
# Refresh the github.com/teacheramitk/git-demo and see first commit
$ git add .
$ git status
$ git push 
$ git commit -m "second commit"
$ git push 
# Refresh the github.com/teacheramitk/git-demo and see second commit
```
### End of lab



# Create a remote Github repository & Clone it locally - Lab

**Step 1.Goto www.github.com**

**Step 2. Click on "+" sign and click on New repository**

**Step 3. Give name of repository "git-demo-1"**
- Select Public
- Select Add a README file

Click on Create repository
 
**Step 4. teacheramitk/git-demo-1>Code>Clone**
- Copy the URL

**Step 5. Open Terminal in Visual Studio Code**
```sh
$ cd Documents/
$ cd Course-Material/
$ git clone https://github.com/teacheramitk/git-demo-1.git
# Check by opening in the PC
$ touch .gitignore
# Write .DS_Store in .gitignore
$ git status
$ git add .
$ git commit -m "first commit"
$ cat .git/config
$ git push
# Refresh the github.com/teacheramitk/git-demo and see .gitignore commit
```
### End of lab


# AWS CodeCommit : Create and set-up CodeCommit Repo- Lab

**Step 1. Goto AWS Management Console>Services>Developer Tools>CodeCommit**

**Step2. Click on Create Repository**

**Step 3. In Repository settings give Repository name as "Sample-Node-App"**

Click on Create

**Step 4. Repository created successfully now Goto IAM Concole**

**Step 5. Goto AWS Management Console>Services>IAM**

**Step 6.Click on Users>Amit> Security credentials>HTTPS Git credentials for AWS CodeCommit**
 - Click on Generate credentials>Download Credentials
 - Click on Close
 
**Step 7.Goto AWS Management Console>Services>Developer Tools>CodeCommit>Repositories>Sample-Node-App**
 - Click on Clone URL>Clone HTTPS
 - Come down to Step 3:Clone the repositrory
   - Click on Copy
   
 **Step 8. Open Visual Studio Code>New Terminal**
 - Type the following commands
```sh
$ cd Documents/
$ cd Course-Material/
# Paste the Clone repositrory copied in Step7
$ git clone https://git-codecommit.ap-south-1.amazonaws.com/v1/repos/Sample-Node-App
# Provide AWS Credentials (User name and Password)
# After Cloning open this repository in VS Code
# Open Terminal and check for git initialization
$ git status
```

### End of Lab



# AWS CodeCommit : Push Sample NodeJS App on CodeCommit Repo - Lab

**Step 1. Open Visual Studio Code>New Terminal**
- Type the following commands
```sh
$ touch .gitignore
# Click on .gitignore and see two files to ignore node_modules/ & >DS_Store
$ git status
$ git add .
$ git status
$ git commit -a "first commit"
$ git push
```
**Step 2. Goto AWS Management Console>Services>Developer Tools>CodeCommit>Repositories>Sample-Node-App**
- gitignore has node_modules/ & >DS_Store
- Click on Commits and see the first commit there

**Step 3.Goto Visual Studio Code>Terminal**
```sh
$ cp -r ../new-node-project .
$ rm -rf new-node-project
$ cp -r ../new-node-project/ .
$ git status
# Check untracked files
$ git add .
$ git status
$ git commit -m"second commit"
$ git push
```
**Step 3. Goto AWS Management Console>Services>Developer Tools>CodeCommit>Repositories>Sample-Node-App**
- Check that all files have been pushed here
- Goto commits and see that second commit is present there


### End of Lab













