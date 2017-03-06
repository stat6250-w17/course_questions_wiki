# Course Questions Wiki

This document contains questions and answers corresponding to reading from the course textbook.

To contribute,

1. fork this repo to your GitHub Account (e.g., using the "Fork" button in the upper-right-hand corner of the GitHub web interface),

2. make appropriate changes/corrections using Markdown (see https://guides.github.com/features/mastering-markdown/), and

3. initiate a pull request using

- the master branch of the stat6250/course_questions_wiki repo as the base fork and

- your version of the repo as the head fork.

********************************************************************************

## Chapter 1 Questions
*[Chapter 1 , Problem 2 ]
* **Question (SK): Is indentation  crucial in SAS or it is just for readability?If not then why does some programs gives error because of wrong indentation?**
* **Answer (SK) : Writing codes with proper indent is a bset practice for programming.**

## Chapter 2 Questions

[Chapter 2, Problem 7]
- Question (IL): What's the difference between starting a SAS program with "data" versus "proc", and why do both end types of programs end with the same "run" command, even though the bodies of the programs look nothing alike?
- Answer (IL): SAS programs are divided into "steps", each step is either a data step or a proc step (as determined by the first word in the step), and all steps are typically terminated by a "run" statement. However, when using a "cards" or "dataline" statement in a data step, then the data step is terminated by a closing semicolon. In addition, some procs (like the interactive proc glm) are only terminated with a "quit" statement.

[Chapter 2, Problem 9]
- Question (IL): What is a "libref", and how does it differ from a "LIBNAME"?  In particular, what fundamental distinction causes one to be written out in lower-case letters and the other in upper-case letters?
- Answer: TBD

[Chapter 2, Problem 7]
* ** Question (SK)-What is YEARCUTOFF= option? Why is this different in two year and four year naming conventions?**
* ** Answer (SK)-The value of the YEARCUTOFF= system option affects only two-digit year values. A date
value that contains a four-digit year value will be interpreted correctly even if it does not fall within the
100-year span set by the YEARCUTOFF= system option.**


## Chapter 3 Questions
*[Chapter 3 Problem 1]

* **Question (SK):What is the main difference between snippets and abbreviation?**

*  **Answer (SK): Snippets are small piece of code that actually run and can be used in a larger programe.And abbreviation is short hand notation.**

## Chapter 4 Questions
* ** Question(SK)- How can we change the variable type from char to numeric without creating a temporary dataset? **
* ** Answer -TBD

## Chapter 5 Questions
* ** Question(SK)- How we can write an programe that do assignment and increments in a vaiable together in SAS ?**
-Answer-TBD

## Chapter 6 Questions
* ** Question (SK)- DATA step reads values from the file Invent and executes as many times the number of records are there.What if there is a row but value is missing? **
-Answer-TBD

## Chapter 7 Questions


## Chapter 8 Questions
* ** Question (SK)-Does reversing the order of the variables in the TABLES statement would reverse their positions in the table?**

## Chapter 10 Questions


## Chapter 11 Questions
* Question(SK)-Can we create a new variable within a new dataset that is different from the one in set statement?*
* Answer-TBD

## Chapter 12 Questions
* Qusetion (SK)-Does Proc SQL has all the SQL commands ? like for e;g inner and outer join?*
*Answer -TBD

## Chapter 13 Questions


## Chapter 14 Questions


## Chapter 15 Questions


## Chapter 16 Questions


## Chapter 17 Questions


## Chapter 19 Questions


## Chapter 20 Questions
