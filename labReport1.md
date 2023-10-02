# Lab Report #1

## cd:
1.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/27328f9b-5245-4b98-b844-da22a554b55f)
The working directory was originally /home/.
When I ran cd with no arguments with my working directory being /home/ (nothing following "cd" in the terminal) there wasn't any changed in my working directory, files, or terminal.
However, it seems when I'm in another working directory (`[user@sahara ~/lecture1]`) through using "cd ____" (Ex: "cd lecture1") using just "cd" afterwards places my working directory in /home/.
This was not an error. 

2.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/c79a85d6-5349-43bd-9c6a-cd8b2cf37108)
The working directory was originally /home/.
When I ran cd with a folder argument (Ex: "cd lecture1"), my working directory was changed to lecture1 (as seen by `[user@sahara ~/lecture1]`).
Additionally, when I ran cd with another folder argument (Ex: "cd messages"), my working directory was changed to messages (as seen by `[user@sahara ~/lecture1/messages]`)
This was not an error.

3.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/02dca537-f263-426b-bd0c-5af9ae7e8fcc)
The working directory was /home/lecture1.
When I ran cd with a file argument (Ex: "cd Hello.java"), it displayed an error message that stated `bash: cd: Hello.java: Not a directory`.
The same thing happened when my working directory was /home/lecture1/messages; doing a file argument (Ex: "cd en-us.txt") displayed an error message that stated `bash: cd: en-us.txt: Not a directory`.
This is an error, since cd changes the working directory. Therefore, since files aren't a directory, we cannot go into the file using "cd", therefore giving the error message saying that the given file isn't a directory.

## ls:
1.
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/33b03ee6-b491-4922-9e06-bc0e71cf2d42)
