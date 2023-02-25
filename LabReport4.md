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

Running the junit tests inside TestListExamples.java:

``
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples
``

## Identifying and fixing the error:

<br/>

Open the ListExamples.java file to examine:

``
nano ListExamples.java
``

<br/>



