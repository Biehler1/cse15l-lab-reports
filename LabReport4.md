# Lab 4
## Step 4
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/aa38895d-5214-4e54-ad30-7e8539826a5c)

Keys Pressed: `ssh cs15lfa23ad@ieng6.ucsd.edu <ENTER>` I typed this out on my own.

Explanation: The `ssh` command is used to access and manage remote servers and systems. Since the argument was `cs15lfa23ad@ieng6.ucsd.edu`, I am remotely connecting to a computer called `cs15lfa23ad`.

## Step 5
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/f0d6aa5c-6c6a-4f9c-878e-c6a4b12e6d6f)

Keys Pressed: `git clone <CTRL>+<SHIFT>+<P> <ENTER>`. I copy and pasted `git@github.com:Biehler1/lab7.git` where `<CTRL>+<SHIFT>+<P>` is.

Explanation: The `git clone` command is used to clone the contents of a git repository onto the remotely connected machine. The argument `git@github.com:Biehler1/lab7.git` is the address to the repository.

## Step 6
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/c0be939a-799e-4ef3-b6e0-e53cfea49b8b)

Keys Pressed: `cd l <TAB> <ENTER>`. This command filled to be `cd lab7/`, putting me into the lab7 directory. Then, I pressed `<CTRL>+<SHIFT>+<P> <ENTER>`. `<CTRL>+<SHIFT>+<P>` copy and pasted `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`. 
I got this code from the `Week 4 - Testing and Files` lab. Afterwards, I pressed `<CTRL>+<SHIFT>+<P> ListExamplesTests <ENTER>`. `<CTRL>+<SHIFT>+<P>` copy and pasted `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore`. 
I also got that part of the code from the `Week 4 - Testing and Files` lab. Then I typed out the ListExampleTests argument myself.

Explanation: `cd lab7/` changed my directory to lab7. `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` compiles all of the java programs in the lab7 directory with the classpath `.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar`, which means
that the compiler used some of the classes in `.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar` to compile the java programs present in the lab7 directory. `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`
runs the `ListExamplesTest.class` file with the classpath `.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar`, which means that the JVM uses some of the classes present in the jar file to run the program. The other argument `org.junit.runner.JUnitCore`, is the
main class for running and executing JUnit tests from the command line, reporting what tests passed or failed.

## Step 7
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/23a13798-e35e-4a89-b057-a016a9e9e490)
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/9610bfba-31ab-429d-beb4-a9daf3721ee1)
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/3d9ff73b-f45d-44f4-8e0d-4c237aaa8f09)

Keys Pressed: `vim ListExamples.java <ENTER>`. This placed me into the vim editor for the ListExamples.java file. In the vim editor, I typed `<SHIFT>+<DOWN> <SHIFT>+<UP> <SHIFT>+<RIGHT> <UP> <UP> r2 :wq!`.

Explanation: The vim editor allows me to edit the `ListExamples.java` from the remote server. `<SHIFT>+<DOWN>` brought me to the bottom of the `ListExamples.java` and `<SHIFT>+<UP>` takes me to the beginning 'r' of `return result;`. `<SHIFT>+<RIGHT>` takes me
to the 'n' in the `return`, then the two `<UP>`s take me to the '1' in `index1` that needs to be changed. r2 deleted the '1' in index1 and changes it to a '2'. Therefore, creating the result wanted. `:wq!` saves and exits the vim editor.

## Step 8
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/b3095fc2-c75b-4776-a3e1-eb1bd9d7f1bb)

Keys Pressed: `<UP> <UP> <UP> <UP> <UP> <ENTER>`, which ran the `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command. The `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command was 5 up in the remote server's search 
history, so I used the up arrows to access it. Next, I pressed `<UP> <UP> <UP> <UP> <UP> <ENTER>`, which ran the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` command. The command 
`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` was 5 up in the remote server's search history, so I used the up arrow to access it. 

Explanation: `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` compiles all of the java programs in the lab7 directory with the classpath `.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar`, which means
that the compiler used some of the classes in `.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar` to compile the java programs present in the lab7 directory. `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`
runs the `ListExamplesTest.class` file with the classpath `.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar`, which means that the JVM uses some of the classes present in the jar file to run the program. The other argument `org.junit.runner.JUnitCore`, is the
main class for running and executing JUnit tests from the command line, reporting what tests passed or failed. In this case, they all passed.

## Step 9
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/a173c6f6-df3b-448f-a286-9713ac129c0f)

Keys Pressed: I typed all of the commands by hand. `git add . <ENTER>` `git commit -m "Timed Test" <ENTER>`. `git push origin main <ENTER>`. 

Explanation: `git add .` helps stage all of the files in the current directory for the next commit. This essentially means that it processes all of the changes to the repository, and waits for it be committed. `git commit -m "Timed Test"` commits the file
to the git repository. This means that a snapshot of your project is created at a specific point in time to a local git repository with a unique identifier. `git push origin main` adds, or 'pushes', these changed to the main GitHub repository. `origin` is the 
default name assigned to the github repository, and `main` is the name of the branch.
