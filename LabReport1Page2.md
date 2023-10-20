### Second Command: ls

Example of the command with no arguments:

<sup> The output is the result of the command being used to list the files/directories inside the current working directory of the given path. In this case, there was no given path so it listed the contents of the **/home** directory which was the **lecture1** nested directory. (Errors no)
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ ls
lecture1
[user@sahara ~]$ 
```

Example of the command with a path to a directory:

<sup> The output is the command listing the contents of the **lecture1** directory, which are files and directories that are only within it and not any outside files/directories. For example, in the **lecture1** directory, the **ls** command displayed the files that are within it and a directory **messages**, but it only listed the directory name **messages** and not the files that are within that one as well. In order to display those files, we would have to add a second path to it **ls lecture1/messages** in order to list those files within **messages** because it would be another layer/nest added to it. (Errors no)
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
[user@sahara ~]$ 
```

Example of the command with a path to a file:

<sup> The output is just the command printing the path to the file (same as the the given argument) because after the file **ar-sy.txt**, there is no directory or file inside of it to list. Although, if we were to **ls lecture1/messages/ar-sy.txt lecture1**, the command would still print the file path while in the same time, print the lecture1 contents because it's another/seprate argument. (Errors no)
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ ls lecture1/messages/ar-sy.txt
lecture1/messages/ar-sy.txt
[user@sahara ~]$ 
```

