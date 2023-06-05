# Lab Report 5 - Debugging Scenario
In this lab, you see a scenario of a debugging situation between a student and a TA.

---

## Part One: Student Post & TA Response

### Student Post:
*What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?*

I am using the terminal on VS Code via my MacBook to run a `bash` script that mimics Gradescope's autograder. The `bash` script is from week six lab call `List-Examples-Grader`.

*Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.*

The `bash` script called `grade.sh` takes in a repository consistenting of code for the `ListExamples.java` and compiles and runs `JUnit` tests on `ListExamples.java`. However, when running the command `bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-corrected` in my terminal, I get an output of that says the file has not been found as seen in the image below.

![image](NotWork.png)

*Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.*



### TA Response:
not
### Java File & Bash Script:

## Part Two: Reflection
