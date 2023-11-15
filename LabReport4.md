# Timing Tasks
# 4. Log into ieng6
![ieng6-login](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/bdadcdb8-f07f-445d-90e1-7e44af115913)
Keys pressed: `ssh cs15lfa23it@ieng6-201.ucsd.edu <enter>` this logged me into my remote account, and I was able to log in without a password.
# 5. Clone your fork of the repository from your Github account
![clone-the-fork](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/274c5943-4185-4e1f-aa76-211ed8e3b3ed)
Keys pressed: `git clone <Ctrl+V><enter> ls`. I cloned the repository and used `ls` afterward to check that it was successful.
# 6. Run the tests, demonstrating that they fail
![test-fail](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/7099b9a4-6c15-44af-939a-50c6856afe1f)
Keys pressed: `cd lab7<enter>`and `bash test.sh<enter>`. I changed the directory into lab7 and ran `bash test.sh` to demonstrate that not all the tests passed.
# 7. Edit the code file ListExamples.java to fix the failing test (as a reminder, the error in the code is just that index1 is used instead of index2 in the final loop in merge)
![fix-code](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/70f2cbe2-24cc-4aaa-99b7-7537d31ef427)
Keys pressed: `vim ListExamples.java<enter>` when the file opened, my cursor was located right before the 1 on the variable index1, so I pressed `i` to enter insert mode, `<right><backspace>2<esc>:wq`.
I used vim to open and edit the ListExamples.java file.
# 8. Run the tests, demonstrating that they now succeed
![test-passed](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/2fe3e662-944c-4d2f-b210-95399e312c80)
Keys pressed: `bash test.sh<enter>` I used this command again to rerun the tests to demonstrate that they all succeeded.
# 9. Commit and push the resulting change to your Github account
Keys pressed:
![git-push](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/53a96bf1-a21c-424b-883c-03529d6ac1f8)
`git add ListExamples.java<enter>` to stage a file to be part of the next commit, `git commit -m "index1->index2"<enter>` to create a commit locally for all staged files & I used the -m flag to type my commit message within the same command, `git push` to copy all new commits to GitHUb.
