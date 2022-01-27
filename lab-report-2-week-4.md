# Week Two and Three Lab Report

[Index page link](https://abigailshilts.github.io/cse15l-lab-reports/)

[first lab report link](https://abigailshilts.github.io/cse15l-lab-reports/lab-report-1-week-2)

## This report is covering Debugging

### Issue 1 - Infinite loop when extra line is att the bottom of the file

[Go here to find the specific test that caused this error](https://github.com/abigailshilts/markdown-parse-abbi/blob/5b1f7a5b7a70be3e397796f285a626eae257bada/test-extraLine.md)

When the code is ran it ends up with this infinite loop output (I used `ctrl-c` eventually to exit the loop):

![Image](img2/ex1-infiniteLoop.png)

To solve we implemented the following changes:

![Image](img2/ex1-codeDiff.png)

The _bug_ in the program was that it would run so long as the contents of the file being examined were longer than the index of the most recent closing parenthesis +1. This means that any input file that does not end with a closing parenthesis will create the _symptom_ shown above: an infinite loop. Thus to solve for these _failure inducing inputs_ we changed the program to also exit the loop when there are no more closing parenthesis in the file.

