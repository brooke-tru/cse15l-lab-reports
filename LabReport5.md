Symptom: The behavior you see (terminal output, error messages, web page contents)
Bug: A slaw in the program that causes the symptom

1. The original post from a student with a screenshot showing a symptom and a description of a guess at the bug/some sense of what the failure-inducing input is. Describing the bug should involve reading some output at the terminal resulting from running one or more commands. 
![original post](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/15133f6b-861d-4de8-bb3a-848624075226)

2. A response from a TA asking a leading question or suggesting a command to try (To be clear, you are mimicking a TA here.)
TA response: Hi Brooke, I think that your suspicions are a good place to start when it comes to debugging. Let's take it a step further and look at the code in `ListExamples.java`, when you trace the code, what elements get inputted at what index? I hope that's a good starting place for your debugging!

3. Another screenshot/terminal output showing what information the student got from trying that, and a clear description of what the bug is.
![fixed-bug](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/bec5e8aa-082b-45c7-ae66-d657c1d22081)
After hand tracing the code for the merge() method in `ListExamples.java` with a random example, I found out that the second while loop was over-incrementing the `index2` variable. I fixed this by changing the increment value to 1, and the test passed! Thanks for the help.

4. At the end, all the information needed about the setup including:
  * The file & directory structure needed
![file   directory structure](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/8176381e-f19b-4e9d-9c11-bd26a04b6ce4)
![structure](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/eb1b537f-24f5-4231-8ea2-79c5ee432ed9)
  I used the lab 7 code  to setup my scenario. https://github.com/brooke-tru/lab7

  * The contents of each file before fixing the bug
This is the merge() method: ![file-before](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/0fcc65a7-a7a0-4e70-ab2d-f734564348e3)
This is the test that failed located in `test.sh`: ![failing-test](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/11d30048-2f75-4911-af8b-d16c250e0f92)

  * The full command line (or lines) you ran to trigger the bug
`bash test.sh` ran 2 tests, and the merge() method didn't pass the test.
  
  * A description of what to edit to fix the bug
![fix](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/a892a6e0-6fe1-4a1c-9f09-489af45fd69d)
So, the bug was that the `index2` variable was being incorrectly incremented hence the failing test. To fix the incrementing, I changed the value from 2 to 1.

