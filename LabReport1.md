# Week 1 Lab Report
## Step 1: Find Your CSE15L Account
- Go to https://sdacs.ucsd.edu/~icc/index.php to find your CSE15L account, where it should begin with cs15lwi23xxx.
- Now reset the password by clicking your CSE15L account and go to change password.
- Before you create a new password, change the **Change MyTritonLink** to **no** so that it will 
only change your course specified account password.
- The new password could take up to 15 minutes to set in.

## Step 2: VScode
- First, log in one of the computers in the CSE lab.
- Then find and open Visual Studio Code. It should look like this:

![image](https://user-images.githubusercontent.com/122485613/215643148-d904a1f6-093b-4ac7-b43c-9e07e70dd34d.png)

## Step 3: Remote Login
- Now open a terminal in Visual Studio Code and type the command `ssh cs15lwi23xxx@ieng6.ucsd.edu` using your own 
CSE15L account.
- A few messages will appear and at the very end, it will ask `Are you sure you want to continue connecting (yes/no/[fingerprint])?` in where 
you will type `yes` in the command window.
- Then you have successfully login and your screen should look like this:

![image](https://user-images.githubusercontent.com/122485613/215643030-1098ad6f-b08d-4098-82a1-3eac2e8ac9a7.png)

## Step 4: Testing Commands
- Test out the some of commands such as `pwd`, `mkdir`, `ls`, and `cd` and see what each does.
- You should see that:
    * `pwd` stands for "Print Working Directory" and prints out the current working directory.
    * `mkdir [path]`stands for "Make Directory" and creates a new directory from the given path.
    * `ls [path]` stands for "list" and prints out all the files and folders in the given path. (If [path] is empty, then it prints
    from the current directory.)
    * `cd [path]` stands for "Change Directory" and is used to transiton through directories. (Bonus: If [path] is `..` then it will
    change the to the previous directory and if [path] is `~`, then it will move back to the main directory.)
    
![image](https://user-images.githubusercontent.com/122485613/215642539-916041cf-eb8e-42de-8577-0b66d5fd7d9d.png)
