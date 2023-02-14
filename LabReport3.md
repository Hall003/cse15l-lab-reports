# Lab Report 3

## Grep -r
`` grep -r "economic growth" ``
<br/>
<img src="/LabReport3/rEconomic.png">
"grep -r" recursively searches a directory to find files that contain the given pattern. In this case the pattern was "economic growth" and it returned the files and lines that matched the patterns. The first result was longer than the others because it contained multiple lines in a row that contained "economic growth". 
<br/>

`` grep -r "mathematical model" ``
<br/>
<img src="/LabReport3/rMath.png">
Here, the pattern that was recursively searched for in the directory "written_2" was "mathematical model" and only two files matched the pattern. 
<br/>

## Grep -n

`` grep -n "treasure" ./travel_guides/berlitz1/WhereToMalaysia.txt ``
<br/>
<img src="/LabReport3/nTreasure.png">
"grep -n" searches the file for the given pattern and returns the lines and line numbers that match the pattern.  In this case, lines 67, 827, 1609, and 2493 matched the pattern "treasure".
<br/>

`` grep -n "economic" /Users/hall/Desktop/Winter23/CSE15L/docsearch/written_2/non-fiction/OUP/Fletcher/ch6.txt ``
<br/>
<img src="/LabReport3/nEconomic.png">
Here, the pattern that was searched for in Fletcher Ch6 was "economic" and 5 lines in the file matched this pattern. 
<br/>

## Grep -v

`` grep -v "and" /Users/hall/Desktop/Winter23/CSE15L/docsearch/written_2/non-fiction/OUP/Fletcher/ch10.txt ``
<br/>
<img src="/LabReport3/vAnd.png">
The command "grep -v" searches for and returns lines of the file that do **not** contain the given pattern. For this example, it is clear that none of the returned lines contain the word "and".
<br/>
`` grep -v "the" ./travel_guides/berlitz2/China-History.txt ``
<br/>
<img src="/LabReport3/vThe.png">
As shown in this example, the command **is** case sensitive which is why "The" still appears, but "the" does not. And since "the" is a very commonly used line, there are not many lines returned.
<br/>

## Grep -E

`` grep -v "and" /Users/hall/Desktop/Winter23/CSE15L/docsearch/written_2/non-fiction/OUP/Fletcher/ch10.txt ``
<br/>
<img src="/LabReport3/vAnd.png">
The command "grep -v" searches for and returns lines of the file that do **not** contain the given pattern. For this example, it is clear that none of the returned lines contain the word "and".
<br/>
