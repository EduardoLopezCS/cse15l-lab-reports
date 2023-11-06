## Part 2(For command **find**): 

### Two examples for option **-name**:
```
find 911report -name "*.txt"
911report/chapter-13.4.txt
911report/chapter-13.5.txt
911report/chapter-13.1.txt
911report/chapter-13.2.txt
911report/chapter-13.3.txt
911report/chapter-3.txt
911report/chapter-2.txt
911report/chapter-1.txt
911report/chapter-5.txt
911report/chapter-6.txt
911report/chapter-7.txt
911report/chapter-9.txt
911report/chapter-8.txt
911report/preface.txt
911report/chapter-12.txt
911report/chapter-10.txt
911report/chapter-11.txt
```
```
find . -name "chapter-1.txt"
./911report/chapter-1.txt
```
For the first example, the command option **-name** is searching for the specific "name" and it list the files it's associated with. It's useful if the programmer knows the file type(.txt, .java, etc) he or she looking for, making their search more easy. For the second example, I knew the name of the file and the main **technical** directory it's in but not the sub/nested directory it's inside of. With **-name**, I was able to find the sub directory the **"chapter-1.txt"** file was in, which was the **911report** directory.

### Two examples for option **-type**:
```
find . -type d 
.
./government
./government/About_LSC
./government/Env_Prot_Agen
./government/Alcohol_Problems
./government/Gen_Account_Office
./government/Post_Rate_Comm
./government/Media
./plos
./biomed
./911report
```
```
find 911report -type f 
911report/chapter-13.4.txt
911report/chapter-13.5.txt
911report/chapter-13.1.txt
911report/chapter-13.2.txt
911report/chapter-13.3.txt
911report/chapter-3.txt
911report/chapter-2.txt
911report/chapter-1.txt
911report/chapter-5.txt
911report/chapter-6.txt
911report/chapter-7.txt
911report/chapter-9.txt
911report/chapter-8.txt
911report/preface.txt
911report/chapter-12.txt
911report/chapter-10.txt
911report/chapter-11.txt
```
For both examples above, I used the **-type** option for the find command. It is usefull as it list's out specific files or directories depending on the type that you, the programmer, is searching for. For example, the first example is the find command searching and listing all the sub directories within **technical** using the key character **d**. For the second example, I chose a different key character **f** to list all the normal files within the **911report** sub directory. 

### Two examples for option **-size**:
```
find . -size  -1k
.
./government
./government/About_LSC
./government/Env_Prot_Agen
./government/Alcohol_Problems
./government/Post_Rate_Comm
./plos/pmed.0020191.txt
./plos/pmed.0020226.txt
./911report
```
```
find . -size +200k
./government/About_LSC/commission_report.txt
./government/Env_Prot_Agen/bill.txt
./government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
./government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
./government/Gen_Account_Office/d01591sp.txt
./911report/chapter-13.4.txt
./911report/chapter-13.5.txt
./911report/chapter-3.txt
```
Both examples above show the use of the **-size** option for **find**. This option searches for a specific file(s) given a size like 10M(megabytes), 10000k(kilobytes), 2G(gigabytes), etc. It's useful if the programmer knows the size of the files, they can get a list of the ones that accomodate the given size. It also helps to list out the files that are either greater than or less than the given size. The second example listed the larger sized files(greater than 200 kilobytes) than the first example, which were smaller(less than 1 kilobyte) files. 

Outside source: https://www.linuxteck.com/find-command-in-linux-with-examples/
