# Lab Report 5
## Part 1
1. __Title:__ Bug involving JUnit tests

I'm facing an issue when running my bash script. It outputs these errors in the terminal. 
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/53ac9b25-5a9c-4dcd-b2c6-936ec59ed4aa)
Here is the code for my bash script:
```
#Since for windows there are two separate CPATHs for compiling and running JUnit tests.
CPATH1=".;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar"
CPATH2=".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar"

rm -rf student-submission
rm -rf grading-area

mkdir grading-area

git clone $1 student-submission
echo 'Finished cloning'

# Checks if ListExamples.java exists.
# If it doesn't send an error.
if [ ! -e "student-submission/ListExamples.java" ]; then 
    echo "Error: No ListExamples.java file found."
    exit 1
fi

# Copies ListExamples.java, TestListExamples.java, and all JUnit files in lib to grading-area
cp student-submission/ListExamples.java grading-area/
cp TestListExamples.java grading-area/

# Compiles JUnit Tests and sees if there is an error code
# If so, send an error.
cd grading-area
javac -cp $CPATH1 *.java

if [ $? -ne 0 ]; then
    echo "Error: Compilation error."
    exit 1
fi

# Runs JUnit Tests and redirects all output into test-results.txt
java -cp $CPATH2 org.junit.runner.JUnitCore TestListExamples > test-results.txt 2>&1

# Checks if there is any FAILURES!!! from the JUnit test.
# If so, tells the user that tests failed
if grep "FAILURES!!!" test-results.txt; then
    echo "Tests failed. See test-results.txt for details."
else
    echo "All tests passed."
fi
```
I believe the issue is related to a directory issue, since I can run the test cases by itself just fine from the terminal.

2. __TA Response:__ Hi, you're right that this is an issue with the JUnit tests not running. I can't really help right now until I see more of your directory stucture. More specifically, I want to see what is in the grading-area directory.

__Student Response:__ Here is my directory structure: 

![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/c890baeb-0fcc-4ce5-865f-2db67018e67e)

Let me know if you need anymore information!

__TA Response:__ It seems like there is an issue with reaching the `lib` folder in order to run the JUnit test. In order to reach it, you can either `cp` the `lib` folder into `grading-area`, or make it so the `CPATH` variables check the previous directory for the `lib` folder (using `..`).

__Student Response:__ I tried what you recommended with using `cp` to copy the `lib` folder into `grading-area`, but it still gave an error:
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/af882fc6-e125-453d-8c19-3ad8b4c592ea)
The only line I added was `cp lib grading-area/`.

__TA Response:__ Remember that when we `cp` a directory, we need to add `-r` right after the `cp` in order to recursively copy all of the files in the original directory.

__Student Response:__ Thank you! When I changed `cp lib grading-area/` to `cp -r lib grading-area/`, it worked, giving me this output:
![image](https://github.com/Biehler1/cse15l-lab-reports/assets/103413662/b458bef0-b042-4d96-a87e-ce8970679d60)
Since `list-methods-lab3/` was supposed to fail, this means that now my bash script seems to work!

## Part 2
I think something cool that we learned was about the jdb. This is because back when I took AP Computer Science Principles in High School, the website (code.org) we coded on had a built in debugger that would go line by line through the code. In this 
debugger you could implement "watchers" which would store the values of any variable you wanted and would show if and when they got updated in the code. It made debugging a lot easier. However, when I got to AP Computer Science A, this debugger 
wasn't present at all, and I thought that it was just a thing that code.org had implemented themselves and not something built into some coding languages. I thought this for 2 years straight until we started to learn about jdb in this class.
Therefore, just due to prior experience, and understanding how useful a debugger is when trying to fix code, I thought it was really cool that Java, C, and C++ have their own built in debugger, which also (most likely) implies that other popular
coding languages also contain a built in debugger. 











