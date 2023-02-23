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

Cloning new copy:

  ``
  git clone git@github.com:Hall003/lab7.git
  ``
  
## Running Tests

<br/>

``
cd lab7
``

<br/>

``
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
``

<br/>

``
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples
``
