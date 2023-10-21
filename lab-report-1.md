Lab Report 1
============
_Enrique Aranda_


__cd__
1. No argument
```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$ 
```
The working directory was on `lecture1`. There was no output but now the directory is set to `\home`. No output means this command was not an error.

2. Directory argument
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ 
```
The working directory changed from `/home` to lecture1. There was no output because the command does not return an output when changing the directory. No output means this command was not an error.

2. File argument
```
[user@sahara ~/lecture1]$ cd Hello.java
bash: cd: Hello.java: Not a directory
```
The working directory was on `lecture1`. The output returned was stating that the file that was inserted as an argument, is not a directory. The output of this command is an error because `Hello.java` is not a directory.

---
__ls__
1. No argument
```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
```
The working directory was on `lecture1`. The command prints out a list of all the files/paths in the `lecture1` directory. The output of this command was not an error, the command works as intended.

2. Directory argument
```
[user@sahara ~/lecture1]$ ls /home
lecture1
```
The working directory was on `lecture1`. The argument was for the `/home` directory, therefore the output was the list of all the files in `/home`. The output of this command was not an error, the command works as intended.

3. File argument
```
[user@sahara ~/lecture1]$ ls Hello.java
Hello.java
```
The working directory was on `lecture1`. The argument was for the `Hello.java` path, therefore the output was the list of all the files in `Hello.java`, which is just `Hello.java`. The output of this command was not an error, the command works as intended.

---
__cat__
1. No argument
```
[user@sahara ~/lecture1]$ cat
```
The working directory was on `lecture1`. The output is whatever the user types in after using the cat command. The output of this command is not an error, the command works as intended.

2. Directory argument
```
[user@sahara ~/lecture1]$ cat messages
cat: messages: Is a directory
```
The working directory was on `lecture1`. The output returned states that the messages directory is indeed a directory. The output of this command is an error because it cannot print out a directory.

3. File argument
```
[user@sahara ~/lecture1]$ cat messages/en-us.txt
Hello World!
```
The working directory was on `lecture1`. The output returned is the code of the message in English found in `messages/en-us.txt`, since that file was the argument. The output of this command was not an error, the command works as intended.
