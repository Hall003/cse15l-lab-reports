# Lab Report 4

<br/>


## Set Up

<img src="LabReport4/WhereToFork.png"/>

Click here to fork the repo

<img src="LabReport4/Forking.png"/>

<img src="LabReport4/SSHClone.png"/>

Click on Code and SSH to copy the SSH link

<br/>

Logging in:

<img src="LabReport4/RemoteLogIn.png"/>

  ``
  ssh cs15lwi23apr@ieng6.ucsd.edu
  ``
  
<br/>

Deleting any existing copies:

<img src="LabReport4/RemoteLS1.png"/>
<img src="LabReport4/RemoveLab7.png"/>

  ``
  rm -rf ~/lab7
  ``
  
<br/>

Cloning the forked repo:

<img src="LabReport4/GitCloneLab7.png"/>

  ``
  git clone git@github.com:Hall003/lab7.git
  ``
  
## Running Tests

<br/>

Changing directory to the cloned repo:

<img src="LabReport4/CdIntoLab7.png"/>

``
cd lab7
``

<br/>

Compiling the java files and running JUnit tests for ListExamplesTests.java:

<img src="LabReport4/JUnitFail.png"/>

```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java

java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```

## Identifying and fixing the error:

<br/>

Open the ListExamples.java file to examine:

<img src="LabReport4/Nano.png"/>

``
nano ListExamples.java
``

<br/>

Use the arrow keys to go down 42 lines  

<img src="LabReport4/Nano42Down.png"/>

and then 12 spaces to right,

<img src="LabReport4/NanoPointer.png"/>

press delete once and replace the 1 with a 2 so that the line reads "index2 += 1;"

<img src="LabReport4/NanoDelete.png"/>
<img src="LabReport4/Nano2Num.png"/>

Press control O to save the changes and then control X to exit nano

<img src="LabReport4/NanoO.png"/>

Now we can see that the JUnit tests are all passed:

<img src="LabReport4/JUnitPass.png"/>

## Committing and pushing to GitHub


First add the files to the commits, then set the commit message, and push to origin

<img src="LabReport4/GitCommitPushYay.png"/>

