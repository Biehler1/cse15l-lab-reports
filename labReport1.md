# Lab Report #1

## cd:
1.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/27328f9b-5245-4b98-b844-da22a554b55f)
The working directory was originally /home/.
When I ran cd with no arguments with my working directory being /home/ (nothing following "cd" in the terminal) there wasn't any changed in my working directory, files, or terminal.
However, it seems when I'm in another working directory (Ex: `[user@sahara ~/lecture1]`) through using "cd ____" (Ex: "cd lecture1") using just "cd" afterwards places my working directory in /home/.
This was not an error. 

2.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/c79a85d6-5349-43bd-9c6a-cd8b2cf37108)
The working directory was originally /home/.
When I ran cd with a directory argument (Ex: "cd lecture1"), my working directory was changed to lecture1 (as seen by `[user@sahara ~/lecture1]`). Additionally, when I ran cd with another directory argument (Ex: "cd messages"), my working directory was changed to messages (as seen by `[user@sahara ~/lecture1/messages]`)
This was not an error.

3.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/02dca537-f263-426b-bd0c-5af9ae7e8fcc)
The working directory was /home/lecture1.
When I ran cd with a file argument (Ex: "cd Hello.java"), it displayed an error message that stated `bash: cd: Hello.java: Not a directory`. The same thing happened when my working directory was /home/lecture1/messages; doing a file argument (Ex: "cd en-us.txt") displayed an error message that stated `bash: cd: en-us.txt: Not a directory`.
This is an error, since cd changes the working directory. Therefore, since files aren't a directory, we cannot go into the file using "cd", therefore giving the error message saying that the given file isn't a directory.

## ls:
1.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/33b03ee6-b491-4922-9e06-bc0e71cf2d42)
The working directory was /home/.
When I ran ls with no arguments while my working directory was /home/ (nothing following "ls" in the terminal) it listed out the directory "lecture1" in blue. The reason for this, is because the only file or directory present in /home/ was the directory "lecture1", therefore, when ls lists out all files and directories, only "lecture1" was listed out.
This was not an error.

2.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/a03c4df4-9dca-41c5-8f7b-764aa878d44c)
The working directory was /home/.
When I ran ls with a directory argument (Ex: "ls lecture1"), it listed out all files (Hello.class, Hello.java, README) in regular text and directories (messages) in bolded blue. The same thing happened when I inputted multiple arguments (Ex: "ls lecture1 lecture1/messages), except this time it listed out all files and directories in both directories and was categorized through the name of the directory (Ex: For the lecture1 directory it printed "lecture1:" in the terminal before listing out all of the files and directories). 
This was not an error.

3.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/0ae6c600-5f9d-4cde-b79f-ad448e0bc6a4)
The working directory was /home/.
When I ran ls with a file path as an argument (Ex: "ls lecture1/Hello.java" or "ls lecture1/messages/en-us.txt") all that was listed out in the terminal was the pathway that was inputed (Ex: "lecture1/Hello.java" and "lecture1/messages/en-us.txt" respectively). This was because the only files or directories present when giving the file path as an argument is that specific file, therefore all that is printned out is the file's path.
This was not an error, since when I typed in "ls lecture1/nsald" (a nonexistent file) it gave an error message saying `ls: cannot access 'lecture/nsald': No such file or directory`.

## cat:
1.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/a9e5b4f8-101f-4afd-99a2-de73ef0206e2)
The working directory was /home/
When I ran cat with no arguments (nothing following "cat" in the terminal) the terminal took in my inputs and printed them out exactly the same afterwards (Ex: "Hello???" appears twice although I only typed it once). This appears to be an added functionality of cat for when no arguments are used.
This was not an error.

2.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/c4de49cc-ed0f-4cfa-8da6-0d83853196f6)
The working directory was /home/.
When I ran cat with a directory argument (Ex: "cat lecture1" or "cat lecture1/messages"), it displayed an error message that stated `cat: lecture1: Is a directory` and `cat: lecture1/messages: Is a directory` respectively. The reason this happened was because cat is supposed to print out the text within a file, and since directories aren't files, it gives an error.
This is an error, since cat prints out text within a file, and the path I was using led to a directory. As a result, it gave an error message saying that the given path used was a directory.

3.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/15d2cfc8-d99e-4680-9e78-f415c96105ae)
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/77d36d28-e568-4c06-bb40-e92c2dc87a10)
The working directory was /home/
When I ran cat with a file argument (Ex: "cat lecture1/Hello.java" or "cat lecture1/messages/en-us.txt"), it printed out all of the text written inside the file into the terminal (Ex: For "cat lecture1/Hello.java" it printed out all of the code present in the file). Additionally, cat worked to concatenate multiple files together when two or more arguments were used together (Ex: "cat lecture1/Hello.java lecture1/messages/en-us.txt" printed out contents of both files).
This was not an error. 
