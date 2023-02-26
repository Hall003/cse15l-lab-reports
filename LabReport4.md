# Lab Report 4

<br/>

## Set Up

<br/>
Logging in:

  ``
  ssh cs15lwi23apr@ieng6.ucsd.edu
  ``
  
<br/>

Deleting any existing copies:

  ``
  rm -rf ~/lab7
  ``
  
<br/>

Cloning the forked repo:

  ``
  git clone git@github.com:Hall003/lab7.git
  ``
  
## Running Tests

<br/>

Changing directory to the cloned repo:

``
cd lab7
``

<br/>

Compiling the java files in the directory:

``
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
``

<br/>

Running the junit tests inside ListExamplesTests.java:

``
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
``

## Identifying and fixing the error:

<br/>

Open the ListExamples.java file to examine:

``
nano ListExamples.java
``

<br/>

Use the arrow keys to go down 42 lines and then 12 spaces to right, press delete once and replace the 1 with a 2 so that the line reads "index2 += 1;"

Press control O to save the changes and then control X to exit nano



