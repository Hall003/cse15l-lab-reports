# Lab Report 3

## Grep -r
I asked ChatGPT "what are the commands that can be used with grep" and chose -r
<br/>
The command -r can be useful if you want to find all of the files in a directory that contain a certain pattern. An example could be if you are working on a biology research project and were looking for all of the files containing the name of the disease you're researching. It's important to note that it can find patterns inside of words/character sequences.
<br/>
`` grep -r "economic growth" ``
<br/>
<img src="LabReport3/rEconomic.png">
"grep -r" recursively searches a directory to find files that contain the given pattern. In this case the pattern was "economic growth" and it returned the files and lines that matched the patterns. The first result was longer than the others because it contained multiple lines in a row that contained "economic growth". 
<br/>

`` grep -r "mathematical model" ``
<br/>
<img src="LabReport3/rMath.png">
Here, the pattern that was recursively searched for in the directory "written_2" was "mathematical model" and only two files matched the pattern. 
<br/>

## Grep -n
I asked ChatGPT "what are the commands that can be used with grep" and chose -n
<br/>
This command could be useful if you needed to find a particular name in a file and the context in which it was found. For example, if you are looking at a list of student IDs and need to find the lines of every ID that contains the number sequence "289". It's important to note that it can find patterns inside of words/character sequences.
<br/>
`` grep -n "treasure" ./travel_guides/berlitz1/WhereToMalaysia.txt ``
<br/>
<img src="LabReport3/nTreasure.png">
"grep -n" searches the file for the given pattern and returns the lines and line numbers that match the pattern.  In this case, lines 67, 827, 1609, and 2493 matched the pattern "treasure".
<br/>

`` grep -n "economic" /Users/hall/Desktop/Winter23/CSE15L/docsearch/written_2/non-fiction/OUP/Fletcher/ch6.txt ``
<br/>
<img src="LabReport3/nEconomic.png">
Here, the pattern that was searched for in Fletcher Ch6 was "economic" and 5 lines in the file matched this pattern. 
<br/>

## Grep -v
I asked ChatGPT "what are the commands that can be used with grep" and chose -v
<br/>
This command is useful in scenarios where you want to find all lines that do not contain a pattern. For example, if you are reading a paper that contains a list of artists and a description of their work, but you don't want to see the ones that make contemporary art, you can use -v "contemporary art" to see all other artists.
<br/>
`` grep -v "and" /Users/hall/Desktop/Winter23/CSE15L/docsearch/written_2/non-fiction/OUP/Fletcher/ch10.txt ``
<br/>
<img src="LabReport3/vAnd.png">
The command "grep -v" searches for and returns lines of the file that do **not** contain the given pattern. For this example, it is clear that none of the returned lines contain the word "and".
<br/>
`` grep -v "the" ./travel_guides/berlitz2/China-History.txt ``
<br/>
<img src="LabReport3/vThe.png">
As shown in this example, the command **is** case sensitive which is why "The" still appears, but "the" does not. And since "the" is a very commonly used line, there are not many lines returned.
<br/>

## Grep -E

I asked ChatGPT "what are the commands that can be used with grep" and chose -E
https://www.digitalocean.com/community/tutorials/using-grep-regular-expressions-to-search-for-text-patterns-in-linux
<br/>
This example is useful if you want to find more complex sequences of characters inside a file. It also allows you to search for multiple patterns at once. It's important to note that it can find patterns inside of words/character sequences. Extended regular expressions are kind of confusing, but they are very useful.
<br/>
`` grep -E "[Ww]est" ./travel _guides/berlitz2/China-History.txt ``
<br/>
<img src="LabReport3/EFirst.png">
The command "grep -E" searches for the given pattern based on extended regular expressions. Here, the matches could be inside of other words as long as they followed the given pattern of "West" or "west".
<br/>
`` grep -E "[d]{2}" ./non-fiction/OUP/Fletcher/ch10.txt ``
<br/>
<img src="LabReport3/ESecond.png">
In this example, the command returns parts of the file that contain sequences of 2 "d"s in a row. This could have also been written as "[dd]", but this way utilizes the formatting of extended regular expressions. Another way is [AEIOUaeiou]{2} which would return sequences of 2 repeating vowels, but that would return too many lines for all results to be visible in the terminal.
<br/>
