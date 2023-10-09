### Second Command: ls

Example of the command with no arguments:

<sup> The output is the result of the command being used to list the current directory of the given path. In this case, there was no given path so it listed the contents of the **/home** directory which was the **lecture1** nested directory. (Errors no)
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ ls
lecture1
[user@sahara ~]$ 
```

Example of the command with a path to a directory:

<sup> The output is the command listing the contents of the **lecture1** directory, which are files and nested directories within it. (Errors no)
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
[user@sahara ~]$ 
```

Example of the command with a path to a file:

<sup> The output just prints the path to the file (same as the the given argument) because after the file, there is no directory or file to list. (Errors no)
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ ls lecture1/messages/ar-sy.txt
lecture1/messages/ar-sy.txt
[user@sahara ~]$ 
```

