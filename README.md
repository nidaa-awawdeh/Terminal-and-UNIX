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

#### Part II

<hr>

### Permissions and Links

### Permissions, Redirection, and Piping Exercise

#### Part I (Permissions and links)

1-Create a file called restricted.txt. <br>
**touch restricted.txt** <br>
2-Change the permissions on the restricted.txt file to allow the owner to read and write to the restricted.txt file. Do this using the Octal Notation. <br>
**chmod 600 restricted.txt**
3-Change the permissions on the restricted.txt file to only allow the owner, group and everyone to read and write and execute the restricted.txt file. Do this using the Symbolic notation.<br>
**chmod a+rwx restricted.txt** <br>
4-Create a folder called secret_files. Inside the secret_files folder create a file called first_secret.txt and another folder called classified. Inside of the classified folder create a file called super_secret.txt.<br>
**mkdir secret_files<br>**
**touch secret_files/first_secret.txt<br>**
**mkdir secret_files/classified<br>**
**touch secret_files/classified/super_secret.txt**

5-Change the permissions on the secret_files to only allow the owner and group to read, write and execute in all the files and folders inside of secret_files. Do this using the Octal Notation <br>
**chmod -R 770 secret_files**<br>
6-Create a hard link for the restricted.txt called hard_link.<br>
**ln restricted.txt hard_link**<br>
7-Create a symbolic link for the classified folder called classified_link.<br>
**ln -s secret_files/classified classified_link**

<hr>

 ### Part II
 1-Sort vegetables.txt.<br>
 **sort vegetables.txt** <br>
 2-Count the number of lines in vegetables.txt.<br>
 **wc -l vegetables.txt** <br>
 3-Create a file called vegetables_sorted.txt which contains all the unique, vegetables sorted in ascending order in vegetables.txt (do this without the touch command)<br>
 **cat vegetables.txt | sort | uniq > vegetables_sorted**
 4-Create a file called last_three.txt which contains the last three vegetables in the vegetables.txt file (do this without the touch command).<br>
 **cat vegetables.txt | tail -n 3 > last_three.txt**<br>
 5-Create a file called last_three.txt which contains the last three vegetables in the vegetables.txt file (do this without the touch command).<br>
 **cat vegetables.txt | tail -n 3 > last_three.txt**<br>
 6-Count the number of lines the word "Broccoli" appears on (using wc and grep).<br>
 **cat vegetables.txt | grep "Broccoli" | wc -l**

 <hr>

  #### Intermediate Terminal Exercises.
  
  
