# Lab Report 5

## Optimizing Week 7 Lab and [Lab Report 4](https://hall003.github.io/cse15l-lab-reports/LabReport4.html)

I will be splitting up the bash scripts into two parts, step 1 and step 2. Step 1 covers steps 5 and 6 of our week 7 lab. And Step 2 covers steps 7 through 9 of our week 7 lab. This is to clearly show when the JUnit tests fail and when they succeed after fixing the bug.

### Step 1: Fork the repo

If you already have a copy of lab7 in your github, you will need to delete it.
<br>
Go to lab7 settings
<br>
![Screen Shot 2023-03-12 at 6 05 20 PM](https://user-images.githubusercontent.com/122586453/224586264-8a585b7a-d011-4b77-9e48-b863d201534b.png)
<br>
Then scroll down to the very bottom of general
<br>
![Screen Shot 2023-03-12 at 6 06 41 PM](https://user-images.githubusercontent.com/122586453/224586350-887b88c6-e155-4a4e-9f55-ff2481d88021.png)
<br>
Click on "Delete this repository" and follow the instructions
<br>
![Screen Shot 2023-03-12 at 6 07 31 PM](https://user-images.githubusercontent.com/122586453/224586404-cff66065-fca5-4146-85c9-0b717feb0abe.png)
<br>
Now, you can go back to the repo of lab7 that you were given to clone, [here is the link if you need it](https://github.com/ucsd-cse15l-w23/lab7)
<br>
Press "fork" and then press "create fork" when prompted
<br>
<img src="/LabReport4/WhereToFork.png">

![Screen Shot 2023-03-12 at 6 12 48 PM](https://user-images.githubusercontent.com/122586453/224586835-3708daf5-1e55-4410-abb6-be30e53eaaf7.png)

<img src="LabReport4/Forking.png"/>

### Step 2: Copy the repo link

<img src="/LabReport4/SSHClone.png" height="75%" width="75%">

### Step 3: Remote Log In (XYZ to be replaced by whatever 3-letter combination is in your log in)

Open your terminal and type the following command:
<br>

``
  ssh cs15lwi23XYZ@ieng6.ucsd.edu <enter>
``
![Screen Shot 2023-03-12 at 4 20 13 PM](https://user-images.githubusercontent.com/122586453/224580153-02bc363b-7eed-490a-87aa-1d8eaaaedbf9.png)

### Step 4: Creating the first Bash Script

For this bash script, we want to combine the command that makes sure that there are no pre-existing copies of 
lab 7 already downloaded, the command that clones lab7 onto the remote machine, and 
the commands that run JUnit tests on lab7
<br>
<br>
Run the following command: 
<br>
``
touch step1.sh <enter>
``
Touch searches for the file and if it's not found, it creates the file.
<br>
Run the following command:
<br>
``
nano step1.sh <enter>
``
Nano opens the file so it can be edited.
#### Type out the following code snippets in step1.sh:
Line 1 removes any pre-existing copies of lab7:
<br>

``
rm -rf ~/lab7 <enter>
``

<br>
Line 2 clones the repo onto the local machine (the link should be replaced by the link you copied earlier):
<br>

``
git clone git@github.com:Hall003/lab7.git <enter>
``

<br>
Line 3 changes the working directory to lab7:
<br>

``
cd lab7 <enter>
``

<br>
Line 4 compiles lab7's java files:
<br>

``
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter>
``

<br>
Line 5 runs JUnit tests on ListExamplesTests:
<br>

``
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests <enter>
``
<br>
Press Ctrl+O to save and press Enter to confirm changes
<br>
Your file should look like this:
![Screen Shot 2023-03-12 at 4 33 10 PM](https://user-images.githubusercontent.com/122586453/224580727-1b7fba06-b603-4b32-bdff-3c11c2bdae7d.png)
<br>
Then, to exit, press Ctrl+X

### Step 5: Creating the second Bash Script

For this bash script we want to edit the ListExamples.java files, re-run the JUnit tests, and commit then push the
updated file to our forked repo
<br>
<br>
Run the following command: 
<br>
``
touch step2.sh <enter>
``
Touch searches for the file and if it's not found, it creates the file.
<br>
Run the following command:
<br>
``
nano step2.sh <enter>
``
Nano opens the file so it can be edited.
#### Type out the following code snippets in step2.sh:

Line 1 changes the working directory to lab7
<br>

``
cd lab7 <enter>
``

<br>
Line 2 uses the sed command to edit ListExamples.java to fix the error
<br>

``
sed -i '43s/index1 += 1;/index2 += 1;/' ListExamples.java <enter>
``

<br>
Line 3 compiles the java files in lab7
<br>

``
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java <enter>
``

<br>
Line 4 runs JUnit tests on ListExamplesTests
<br>

``
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests <enter>
``

<br>
Line 5 adds ListExamples.java to the staging area
<br>

``
git add ListExamples.java <enter>
``

<br>
Line 6 commits the file from the staging area and sets the commit message
<br>

``
git commit -m "Updated" <enter>
``

<br>
Line 7 pushes the committed file to the main branch
<br>

``
git push origin main <enter>
``
<br>
Press Ctrl+O to save and press Enter to confirm changes
<br>
Your file should look like this now:
![Screen Shot 2023-03-12 at 4 46 56 PM](https://user-images.githubusercontent.com/122586453/224581414-0fa714bd-bf02-44f1-b3f5-21a0ac4a3998.png)
<br>
Then, to exit, press Ctrl+X

### Step 6: Testing out the scripts

To test step1.sh, type the following command:
<br>

``
bash step1.sh <enter>
``

<br>

![Screen Shot 2023-03-12 at 5 34 47 PM](https://user-images.githubusercontent.com/122586453/224584186-e3b4777a-2348-4bc9-8fa0-881ff2a681a4.png)

Here, we can see that lab7 was cloned from the repo and one JUnit test failed.

<br>

To run step2.sh, type the following command:

<br>

``
bash step2.sh <enter>
``

<br> 

![Screen Shot 2023-03-12 at 5 37 01 PM](https://user-images.githubusercontent.com/122586453/224584326-2ca0c303-89f0-4415-9614-df8f61182599.png)

Here, we can see that all JUnit tests pass and that the fixed file was pushed to main.

<br>

If we check our repo we can see that the ListExamples.java file has been updated:

<br>

![Screen Shot 2023-03-12 at 5 47 17 PM](https://user-images.githubusercontent.com/122586453/224584999-f15efdad-4a77-4b32-80f8-117850d1bee6.png)

### Step 7: Logging out

Now that we're done with our task, we can log out of ieng6. To do so, run the following command:
<br>

``
exit <enter>
``
<br>

![Screen Shot 2023-03-12 at 5 49 26 PM](https://user-images.githubusercontent.com/122586453/224585168-a4b281b3-3c95-47a6-a1eb-f19a93860e65.png)
