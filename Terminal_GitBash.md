# Terminal_GitBash
1) To see where I'm
+ `pwd`

2) Create a folder
+ `mkdir` foldername

3) Go to folder
+ `cd` foldername

4) Create 3 folders
+ `mkdir` foldername1 foldername2 foldername3
+ `mkdir` foldername{1,2,3}
+ `mkdir` foldername{1..3}

5) Go to any folder
+ `cd` foldername1

6) Create 5 files (3 txt, 2 json)
+ `touch` file1.txt file2.txt file3.txt file4.json file5.json
+ `touch` file{1,2,3}.txt file{4,5}.json

7) Create 3 folders
+ `mkdir` foldername_{1..3}

8) Show a list of folder contents
+ `ls` 			- shows the contents of the current folder
+ `ls -f`		- shows the contents of the current folder including deleted files
+ `ls -l`		- shows the contents of the current folder structured, except for hidden ones
+ `ls -a`		- shows the contents of the current folder
+ `ls -l -a`		- shows the contents of the current folder expanded (permissions, owner, size, modified date)
+ `ls -la`		- the same, but shorter
+ `ls ..` 		- shows the contents of the folder above without exiting the current one
+ `ls -lt`		- shows the contents of the current folder sorted by file creation date
+ `ls -lu`		-shows the contents of the current folder sorted by the date the files were accessed
+ `ls -lt`	 	- shows the contents of the current folder sorted by the date the file was created
+ `ls /c/foldername/foldername1` - shows the contents of the folder foldername1 along the path without leaving the current one

9) Open any txt file
+ `vim` file1.txt

10) Write any text to the created file.
+ press `"i"` to be able to enter (edit) the data

+ Write "Lorem ipsum dolor sit amet, consectetur adipiscing elit,
	sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
	Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
	nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
	reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
	pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
	culpa qui officia deserunt mollit anim id est laborum"

11) Save entered data and exit
+ press `"esc"`enter `:wq`

12) Exit folder one level up
+ `cd ..`

13) Move any 2 files you have created to any other folder.
+ `mv` foldername1/{file1.txt,file4.json} foldername1/foldername_3

14) Copy any 2 files you have created to any other folder.
+ `cp` foldername1/{file2.txt,file5.json} foldername1/foldername_2

15) Find file by its name
+ `find . -name` "file1.txt" 		- if we know the file format
+ `find . -name` "file1.*"		- if we don't know the file format

16) View file content in a real time
+ `tail -f` file1.txt - output the contents of the file and its subsequent changes to the console
+ `tail -f` file1.txt | `grep --line-buffered` laborum >> file_log.txt - write changes to a text file after "laborum"

17) Output the first 3 lines from a text file
+ `head -3` file1.txt

18) Output the last 3 lines from a text file
+ `tail -3` file1.txt

19) View the contents of a long file.
+ `less` file1.txt
+ press `q` to exit view mode

20) Display date and time
+ `date`

Tasks *
```
1) Send an http request to the server. http://162.55.220.72:5005/terminal-hw-request
	1) curl "http://162.55.220.72:5005/terminal-hw-request"
	- Response {"Intro":"Hello!! This is your the first response from server","Tasks":{"Task_1"
:"Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_
your_String)&age=(set_your_number)","result":["Your_String","Your_number"]}}
	2)  curl "http://162.55.220.72:5005/get_method?name=(Alona)&age=(25)"
	- Response ["(Alona)","(25)"]
```
```
2) Write a script that will execute the items automatically 3, 4, 5, 6, 7, 8, 13
    1. touch script - create script file
    2. vim script	- open script file for editing
    3. press "i"
    4. enter the name of the shell you are using - #!/bin/bash
    5. enter data:
	* cd foldername
	* mkdir foldername{1..3}
	* cd foldername1
	* touch file{1,2,3}.txt file{4,5}.json
	* mkdir foldername{1..3}
	* ls
	* mv {file1.txt,file4.json} foldername_3
    6. press "esc" enter :wq - save and exit
    7. Make the file executable - chmod +x ./script
    8. Run the script ./script
```


