## Lab Report 1

# cd

**No argument**
```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$ cd
```
When using cd without an argument, if there is a working directory, it is changed back to the home directory, and if the current directory is already the home directory, the command still takes you to the home directory, but there is no change in the working directory since you are already in the home directory.

**Directory as argument**
```
[user@sahara ~]$ cd messages
bash: cd: messages: No such file or directory
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ cd messages
```
When using cd with a directory as an argument, if the working directory is not a parent directory of the argument(and has a parent directory), 
an error occurs as the directory can not be found in the current path. If the working directory is a parent directory of the argument, the working directory is changed to the argument.

**File as argument**
```
[user@sahara ~/lecture1/messages]$ cd en-us.txt 
bash: cd: en-us.txt: Not a directory
```
When using cd with a file as an argument, an error occurs since a file is not a directory, and can not act as a working directory.

# ls

**No argument**
```
[user@sahara ~]$ ls
lecture1
```
When using ls with no argument, the output is the list of all the files and folders in the current path, so in the example, since the working directory is default, only the folder lecture1 is listed

**Directory as argument**
```
[user@sahara ~/lecture1]$ ls messages/
en-us.txt  es-mx.txt  fr.txt  zh-cn.txt
```
When using ls with a directory as an argument, the list of all files and folders directly under the directory are listed, so the 4 txt files in the messages folder are listed in the example.

**File as argument**
```
[user@sahara ~/lecture1/messages]$ ls en-us.txt 
en-us.txt
```
When using ls with a file as an argument, the file itself is listed, as shown in the example.

# cat

**No argument**
```
[user@sahara ~/lecture1]$ cat
hi
hi
```
When using cat without an argument, the terminal accepts user input, and returns the input as an output. In the example above, after typing cat, then typing hi, the cat command returned hi as an output.

**Directory as argument**
```
[user@sahara ~/lecture1]$ cat messages/
cat: messages/: Is a directory
```
When using cat with a directory as an argument, an error occurs, since for the cat command to work properly, a file is expected as an input. So as seen in the example above, there is a message saying the argument is a directory, as the directory messages is not a file. 

**File as argument**
```
[user@sahara ~/lecture1/messages]$ cat es-mx.txt 
¡Hola Mundo!
```
When using cat with a file as an argument, the output is the contents of the file.
