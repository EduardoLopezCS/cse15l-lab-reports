### Second Command: ls

Example of the command with no arguments:

<sup> The output is the result of the command being used to list the current directory of the given path. In this case, there was no given path so it listed the contents of the **/home** directory which was the **lecture1** nested directory.
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ ls
lecture1
[user@sahara ~]$ 
```

Example of the command with a path to a directory:

<sup> The output 
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
[user@sahara ~]$ 
```

Example of the command with a path to a file:

```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ ls lecture1/messages/ar-sy.txt
lecture1/messages/ar-sy.txt
[user@sahara ~]$ 
```

