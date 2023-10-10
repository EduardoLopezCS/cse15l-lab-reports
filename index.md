# **Lab Report 1**
by Eduardo Lopez
### First Command: cd

Example of the command with no arguments:

<sup> The output is the result of the command being used without a directory argument to be changed to, so therefore it doesn't do anything. (Errors no)
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ cd
[user@sahara ~]$ 
```

Example of the command with a path to a directory:

<sup> The output is the command doing it's job, which is changing the current directory to the directory given as an argument. That means instead of starting on the root directory which is **/home** (default), it now starts on the nested one **/lecture1**. (Errors no)
```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ 
```

Example of the command with a path to a file:

<sup> The output is an error because of the result of the command being used on a file path rather than a directory. It doesn't work on files which is why it stated "**Not a directory**". (Errors yes)
```
[user@sahara ~]$ pwd 
/home
[user@sahara ~]$ cd /home/lecture1/messages/ar-sy.txt
bash: cd: /home/lecture1/messages/ar-sy.txt: Not a directory
[user@sahara ~]$
```

