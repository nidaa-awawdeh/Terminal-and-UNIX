# Terminal-and-UNIX

### Navigating in Terminal

###### Questions to Answer

1-What is the difference between / and ~? What do we call each of these directories? <br>
(/)    root directory<br>
(~)    Home<br>
2-What command do we use to change directories? <br>
**cd**<br>
3-What is the difference between an absolute and relative path?   <br>
**relativepath**  where Iam currently<br>
**absolute**   starting from root.<br>

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

#### Part I

1- Create an environment variable called FIRST_NAME and set it equal to your first name (this does not need to be permanent) <br>
**export FIRST_NAME=Nidaa**<br>
2-Print the FIRST_NAME variable<br>
**echo \$FIRST_NAME**<br>
3-Print out the $PATH variable<br>
   **echo $PATH**<br>
4-What is the \$PATH variable?<br>
**It is a set of paths for our environment to find where to run commands** <br>
5-Why would you want to create an environment variable?<br>
**For securing information and using a variable multiple times** <br>
6-How do you permanently save environment variables?<br>
**Save them in your .bash_profile or .zshrc**<br>
7-What is a process?<br>
**a process is a specific computer program that is being excecuted**<br>
8-How do you list all processes running on your machine?<br>
**ps -ax**<br>
9-What is a PID? <br>
**A unique identifier for for a process which is necessary when stopping a process**<br>
10-How do you terminate a process?<br>
**kill or kill -9** <br>
11-What is the difference between kill and kill -9? <br>
**9 is a specific signal ensures that the command can not be ignored, whereas without the -9 there may be processes that are not killed by using kill alone.**<br>
12-What grep flag allows for case insensitive search?<br>**-i** <br>
13-What grep flag allows for a certain number of lines before the match?<br>**-B**<br>
14-What grep flag allows for a certain number of lines around the match?<br>**-C**<br>
15-What grep flag allows for a certain number of lines after the match?<br>**-A**<br>
16-What grep flag allows for full word search?<br>**-w**<br>
17-What grep flag shows you the line number of a match?<br>**-n**<br>

<hr>

#### Part II

1-Find all files inside the Desktop folder that have a name of "learn." <br>
**find ~/Desktop -name "learn"** <br>
2-Find all files inside the Desktop folder that start with a "P."<br>
**find ~/Desktop -name "P.\*" ** <br>
3-Find all files inside the Desktop folder that end with .txt <br>
**find ~/Desktop -name "\*.txt"**
4-Find all files inside the Desktop/views folder that have the name data somewhere in their filename<br>
**find ~/Desktop/views -name "_data_"** <br>
5-Inside of the instructors.txt file, output the number of times the word "Elie" appears.<br>
**grep -c "Elie" instructors.txt** <br>
6-Inside of the instructors.txt file, list all matches for any full word that starts with a capital "P."<br>
**grep -w "P.\*" instructors.txt** <br>
7-Inside of the instructors.txt file, list all the line numbers for any full word that starts with a "z" (it should match regardless of upper or lower case) <br>
**grep -ni "z.\*" instructors.txt**

<hr>
