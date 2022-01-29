# Week 4 Lab Report: Bugs and Symptoms

## 1). Code Change 1

Here is the first code change that we made to try to fix a bug we encountered.
![lab-report-2-images/LR2-1.PNG]

This is a link to the test file we made that broke our initial MarkdownParse.java: [test-file-break.md](https://github.com/rchaklas/markdown-parse/blob/8ab861d0a4ff624217d281dd5b219ff00e05fd33/test-file-break.md).

Here is the symptom of the failure-inducing input as shown in the output:
![lab-report-2-images/LR2-2.PNG]

The symptom in this case is a StringIndexOutOfBounds exception in the output as seen above. The bug is that the program doesn't know how to handle negative values for any of the bracket or parenthesis integers which can be caused by open and closed parenthesis on their own line (failure inducing input). Our code also couldn't handle images, specifically the exclamation mark (another failure inducing input) and would incorrectly see images as links.


## 2). Code Change 2

Here is the second code change that we made to try to fix a bug we encountered.
![lab-report-2-images/LR2-4.PNG]

This is a link to the test file we made that caused the bug: [test-file-break.md](https://github.com/rchaklas/markdown-parse/blob/e2f2996f1812a23313c8ddfdcb0da798768c0366/test-file-break.md).

Here is the symptom of the failure-inducing input as shown in the output:
![lab-report-2-images/LR2-3.PNG]

The symptom in this case was the the 2nd google link to not be displayed in the output when it should be, which was caused by the extra closed brackets (we were unable to fix the closed parenthesis bug, which is unrelated in this case). The bug in our code was that the program didn't know how to handle multiple closed brackets (the failure-inducing input) after the link and so it skipped over it entirely.


## 3). Code Change 3

Here is the third code change that we made to try to fix a bug we encountered.
![lab-report-2-images/LR2-5.PNG]

This is a link to the test file that caused the bug: [test-file8.md](https://github.com/rchaklas/markdown-parse/blob/e003b948d08596c0664bcf8db8b861bb79a867a1/test-file8.md).

Here is the symptom of the failure-inducing input as shown in the output:
![lab-report-2-images/LR2-6.PNG]

The symptom in this case was the StringIndexOutOfBounds exception in the output as seen when our code failed the 8th test case. The bug in our code was the nextOpenBracket becoming negative when we subtract 1 from it in the if statement, which occurs when nextOpenBracket is 0. In this case, the failure-inducing input would be when there is an open bracket on it's own line by itself.

