# Lab Report 4
## My Steps to the Challenge Tasks
### Step 1: Log into ieng6
keys press : `<up><enter>`

![image](https://user-images.githubusercontent.com/122485613/224839233-f12cbea6-116f-47d4-8b16-b35eb9c28eab.png)

The `ssh cs15lwi23aau@ieng6.ucsd.edu` command to log into ieng6 is first in the command history so I just pressed the up arrow
and since I have configured an ssh key from my device, I will automaticaly log in ieng6 without the need of a password.

### Step 2: Cloning my fork of the repository from my Github account
keys pressed : `<up><up><up><up><up><up><up><up><up><up><up><enter>`

![image](https://user-images.githubusercontent.com/122485613/224839352-e4997033-92ed-46b0-89a4-63dfd291daad.png)

The `git clone git@github.com:lplums/lab7.git` command to clone my fork of the lab7 repository again was 11 above in the command
history so I used the up arrow to find this command.

### Step 3: Running the test, expecting a fail
keys pressed: `cd pa7`,`<up><up><up><up><up><up><up><enter>`, `<up><up><up><up><up><up><up><enter>`

![image](https://user-images.githubusercontent.com/122485613/224839592-1d68e471-c922-4885-9ddb-c711ca39dac0.png)

The `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` and 
`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` command are only 7 up in
the command history so I used the up arrow and entered. This will yeild an error.

### Step 4: Edit the code to fix the failing test
keys pressed: `<up><up><up><up><up><up><up><up><up><up><up><enter>` In vim: `<delete>`,`2`,`<escape>`,`:w`,`:q`

![image](https://user-images.githubusercontent.com/122485613/224839792-f70b3303-a12f-44ac-a655-e4671b448e67.png)

In vim:

![image](https://user-images.githubusercontent.com/122485613/224840452-68666bdd-4e00-4edf-b74c-d50c57f42095.png)

The `vim ListExamples.java` will be 11 up in the command history. I found `vim` to be the fastest as I can move the cursor
with my mouse.

### Step 5: Running the test, expecting all test passed
keys pressed: `<up><up><up><enter>` , `<up><up><up><enter>`

![image](https://user-images.githubusercontent.com/122485613/224839885-1d073e7c-161e-425e-ac45-68b05956bf3d.png)

Now we use the `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` and 
`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` command again which is 
only 3 above in the command history as we used it prior. This will now yield a success.

### Step 6: Commit and push the change onto my Githhub account
keys pressed: `<up><up><up><up><up><up><up><up><up><up><up><enter>`, `<up><up><up><up><up><up><up><up><up><up><up><enter>`,
`<up><up><up><up><up><up><up><up><up><up><up><enter>`

![image](https://user-images.githubusercontent.com/122485613/224839926-e00cc2f9-05b2-4528-a951-619aa22f81aa.png)

Lastly, the commands `git add ListExamples.java`, `git commit -m "Updated ListExamples`, and `git push` will all be 11 up in the command history. This will successfully update my repository on my Github account.
  
  
