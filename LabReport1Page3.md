### Third Command: cat

Example of the command with no arguments:

<sup> The command does nothing since there isn't a given argument(path) to a file so that it can do it's job to print out the contents of the file. (Errors maybe) Although, there does seem to be a possible error because after running it, it doesn't reset back to the current working directory but instead, stays in an infinite loop where it prints whatever input the user types into the terminal.
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ cat

```

Example of the command with a path to a directory:

<sup> The output is the command stating that the given argument is a directory. It's considered an error since it only prints out the contents of a given path file and not just from a directory alone. (Errors yes)
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
[user@sahara ~]$ 
```

Example of the command with a path to a file:

<sup> This output demonstrates how **cat** should be used. Giving it an argument path to a file, **cat** prints out the contents like code for example of the given file. If the file doesn't exist, the **cat** command will print out an error stating "**No such file or directory**".  (Errors no) 
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ cat lecture1/messages/en-us.txt
Hello World!
[user@sahara ~]$ 
```
