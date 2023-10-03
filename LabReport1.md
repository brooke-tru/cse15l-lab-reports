# `cd` Command Examples
1. ![cd-no-arguments](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/b8e273cf-da58-4594-85f6-cd6f59dae214)
  The resulting working directory is the home directory after the cd command was run with no arguments. That's because `cd`, which stands for change directory, without any arguments won't do anything because we were basically telling the computer that we don't want any change. This result is no error because we asked the computer to change the directory without any direction, so it did not change from the home directory that it was in. I was able to double check that I was in the home directory by using the pwd command.
2. ![cd-to-directory](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/9692c35b-0ec6-4671-b665-4720ee5772c6)
  I called the cd command with a path to my lecture1 directory. I was in the home directory when I run the code, but after running it with lecture1 as an argument, it changed the directory to lecture1. I got this output beacause the command to change directory with the argument lecture1 changed my directory from home to lecture1. I was able to check this by using the pwd command.
3. ![cd-to-file](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/9191b148-bb14-4143-984f-4461803e4dba)
   I called the 2 cd commands `cd lecture1` and `cd messages` which was the working directory when I proceeded. I called `cd vi-code.txt` which resulted in an error message because it was unable to change the directory because it is "Not a directory". I got this error as a result because I was attempting to `cd` to a file, which is not a valid directory, it is a .txt file. The output is an error, but this is expected due to the previous reason.

# `ls` Command Examples
1. ![ls-no-argument](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/b9631d51-d3ef-413b-889f-ff789170c488)
   I called the `ls` command without any arguments while working in the home directory. The output I was shown was the *lecture1* directory because the `ls` command is meant to show the names of files and folders in the current working directory or to check the current status. I got this output because lecture1 is the only direct folder housed in the home directory. Since there was no argument, the ls command automatically The result is no error because it worked exactly as expected, which was showing the files and folders in the current working directory.
2. ![ls-directory](https://github.com/brooke-tru/cse15l-lab-reports/assets/146862163/baed4f9e-1e18-4191-82c3-c6a19875d2f5)
   I called the command `ls lecture1` while working in the home directory. The output I was shown made sense because all of the listed items are direct files or folders housed in the lecture1 directory. 





