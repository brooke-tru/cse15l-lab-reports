# Part 1 - Bugs
* A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
The buggy code that I chose is the reversed() function.
* Here is the code for the function in ArrayExamples.java:
  
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

* Here is the code from ArrayTests.java & the failure-inducing input from this example is 1,3,5
  
```
  @Test
  public void testReversed1() {
    int[] input1 = { 1, 3, 5 };
    assertArrayEquals(new int[]{ 5, 3, 1 }, ArrayExamples.reversed(input1));
  }
```

* Here is the JUnit test result for this test
  
```
1) testReversed1(ArrayTests)
arrays first differed at element [0]; expected:<5> but was:<0>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
        at org.junit.Assert.internalArrayEquals(Assert.java:534)
        at org.junit.Assert.assertArrayEquals(Assert.java:418)
        at org.junit.Assert.assertArrayEquals(Assert.java:429)
        at ArrayTests.testReversed1(ArrayTests.java:28)
        ... 30 trimmed
Caused by: java.lang.AssertionError: expected:<5> but was:<0>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at org.junit.internal.ExactComparisonCriteria.assertElementsEqual(ExactComparisonCriteria.java:8)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:76)
        ... 36 more
```

* An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
* The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
* Testing the same reversed() function from above in ArrayExamples.java. The input of no input does not induce a failure & here is the code for it from ArrayTests.java:
  
```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

*  Here is the JUnit result which proves that this test doesn't result in a failure:
```
JUnit version 4.13.2
..E...
Time: 0.013
There was 1 failure:
1) testAverageWithoutLowest(ArrayTests)
java.lang.AssertionError: expected:<true> but was:<false>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at ArrayTests.testAverageWithoutLowest(ArrayTests.java:34)

FAILURES!!!
Tests run: 5,  Failures: 1
```

* The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
* Here is the code before the fix:
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

* Here is the code from ArrayExamples.java after fixing it:
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[arr.length - i - 1] = arr[i];
    }
    return newArray;
  }
```
# Part 2 - Researching Commands
* I'm going to research the `find` command
1. `-type` flag source: https://youtu.be/YdL13obmRow?si=xfRpZGOExcYGJrH_
   * `find technical/ -type d` gives the output:
     
```
technical/
technical/911report
technical/biomed
technical/government
technical/government/About_LSC
technical/government/Alcohol_Problems
technical/government/Env_Prot_Agen
technical/government/Gen_Account_Office
technical/government/Media
technical/government/Post_Rate_Comm
technical/plos
```

* The `-type d` flag further specifies what I wanted as a result of directories under the `technical/` folder only.
  This is useful for finding directories within a specific domain that the user can specify themselves
* `find technical/911report -type f` gives the output:
  
```
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
technical/911report/preface.txt
```

* I changed the command to look for files within the path `technical/911report` by using the `-type f` command line option which brings the search results down to files
  within the path that I specified. This is super useful for finding a specific file in a directory.

2. `-name` flag source: https://youtu.be/YdL13obmRow?si=xfRpZGOExcYGJrH_
   * `find technical/911report -name "*.txt"` gives the output:
   
```
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
technical/911report/preface.txt
```

* The `-name` flag matches filenames and directories with the input in double-quotes. In this example, I was trying to find anything within the `technical/911report` path that ended with ".txt".
  This is very useful for finding out what txt files exist within a specific path.
* `find technical/ -name "911report"` gives the output:
  
```
technical/911report
```

* In this example, I was trying to find anything that matched the "911report" input within the technical directory. I was curious if it would give the files within the 911report directory as well, but it only gave the directory itself which is directly under the technical directory. This would be useful for finding the specified directory or file under a path that was given.

3. The `-or` flag source: https://youtu.be/YdL13obmRow?si=xfRpZGOExcYGJrH_
* `find technical/ -name "911report" -or -name "plos"` gives the output:
  
```
technical/911report
technical/plos
```

* In this example, I was trying to find files or directories that lie directly under the technical/ folder with the name "911report" or "plos", since two respective directories exist with those names,
  the output was the paths of those directories. This is useful for further narrowing down a search result in case a user might remember a few options of what their target file or directory is called.
* `find technical/ -name "government" -or -name "biomed"` gives the output:
  
```
technical/biomed
technical/government
```

* In this example, I was trying to find files or directories that lie directly under the technical/ folder with the name "government" or "biomed", since two respective directories exist with those names,
  the output was the paths of those directories. This is useful for further narrowing down a search result in case a user might remember a few options of what their target file or directory is called.
  
4. `-not` flag, source: https://youtu.be/YdL13obmRow?si=xfRpZGOExcYGJrH_
* `find technical/ -type d -not -name "911report"` returns this output:

```
technical/
technical/biomed
technical/government
technical/government/About_LSC
technical/government/Alcohol_Problems
technical/government/Env_Prot_Agen
technical/government/Gen_Account_Office
technical/government/Media
technical/government/Post_Rate_Comm
technical/plos
```
* In this example, I'm trying to find any directory under the technical folder without the name 911report in it. This is useful for users to further narrow down their search result just in case the user remembers
that the name of their target directory certainly cannot be a the specified name in the double quotes.
* `find technical/ -type f -not -name "*.txt"` returns no output because there are no files that exist within the technical folder that do not end with ".txt". This is useful for a user searching for files that aren't txt files. 
