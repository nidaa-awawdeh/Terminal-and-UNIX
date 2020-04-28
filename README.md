# Terminal-and-UNIX

### Navigating in Terminal

###### Questions to Answer

1-What is the difference between / and ~? What do we call each of these directories? <br>
**/** root directory<br>
**~** Home<br>
2-What command do we use to change directories? <br>
**cd**<br>
3-What is the difference between an absolute and relative path?<br>
**relative path** where Iam currently<br>
**absolute** starting from root.<br>

<hr>

### Working with Files and Folders

#### Exercises

1- Create a file called name.txt. <br>
**touch name.txt**<br>
2-Try renaming the file to rename.txt using the mv command. What does this tell you about the command?<br>
**mv name.txt rename.txt** <br>
3-Using the cp command, make a copy of rename.txt and call it copy.txt.<br>
**cp rename.txt copy.txt** <br>
4-Remove the file copy.txt. <br>
**rm copy.txt** <br>
5-Create a folder called questions.<br>
**mkdir questions** <br>
6-Change directories to the questions folder.<br>
**cd questions** <br>
7-Create a file called first.txt.<br>
**touch first.txt** <br>
8-Create a file called second.txt<br>
**touch second.txt** <br>
9-Go back a directory and make a copy of the questions folder and call it questions_copy.<br>
**cp -r questions questions_copy**<br>
10-When using cp -r what is the -r called? What does it do?<br>
**-r <br>
11-Delete the original questions folder and the copy.<br>
**rmdir questions questions_copy\*\*<br>

<hr>

### Terminal Basics Exercises

#### Part I

1-make a directory called first<br>
**mkdir first**<br>
2-change directory to the first folder<br>
**cd first**<br>
3-create a file called person.txt<br>
**touch person.txt**<br>
4-change the name of person.txt to another.txt<br>
**mv person.txt another.txt** <br>
5-make a copy of the another.txt file and call it copy.txt<br>
**cp another.txt copy.txt** <br>
6-remove the copy.txt file<br>
**rm copy.txt** <br>
7-make a copy of the first folder and call it second<br>
**cp -r first second** <br>
8-delete the second folder<br>
**rm -rf second** <br>
