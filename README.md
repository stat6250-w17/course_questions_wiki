# Course Questions Wiki

This document contains questions and answers corresponding to reading from the course textbook.

To contribute,

1. fork this repo to your GitHub Account (e.g., using the "Fork" button in the upper-right-hand corner of the GitHub web interface),

2. make appropriate changes/corrections using Markdown (see https://guides.github.com/features/mastering-markdown/), and

3. initiate a pull request using

- the master branch of the stat6250/course_questions_wiki repo as the base fork and

- your version of the repo as the head fork.

The instructor will then review the pull request and make comments should further revision be needed. Then, after the contents of the pull request have been finalized without any merge conflicts, the instructor will merge the pull request.

********************************************************************************

## Chapter 1 Questions

[Chapter 1, Problem 1]
- Question (SK): Is indentation  crucial in SAS or it is just for readability? If not then why does some programs gives error because of wrong indentation?
- Answer (SK): Writing codes with proper indent is a best practice for programming.

[Chapter 1}
- Question (YM): Is run statement required for every data and proc step?
- Answer (YM): Run statement is not required in every step in SAS program, however having it make every block of statement easier to read and debu.

## Chapter 2 Questions

[Chapter 2, Problem 7]
- Question (IL): What's the difference between starting a SAS program with "data" versus "proc", and why do both end types of programs end with the same "run" command, even though the bodies of the programs look nothing alike?
- Answer (IL): SAS programs are divided into "steps", each step is either a data step or a proc step (as determined by the first word in the step), and all steps are typically terminated by a "run" statement. However, when using a "cards" or "dataline" statement in a data step, then the data step is terminated by a closing semicolon. In addition, some procs (like the interactive proc glm) are only terminated with a "quit" statement.
- Question (SK): What is YEARCUTOFF= option? Why is this different in two year and four year naming conventions?
- Answer (SK): The value of the YEARCUTOFF= system option affects only two-digit year values. A date value that contains a four-digit year value will be interpreted correctly even if it does not fall within the 100-year span set by the YEARCUTOFF= system option.

[Chapter 2, Problem 9]
- Question (IL): What is a "libref", and how does it differ from a "LIBNAME"?  In particular, what fundamental distinction causes one to be written out in lower-case letters and the other in upper-case letters?
- Answer (SG): A libname statement is the syntactical statement used to initiate a particular library. The libref is the actual syntax used to name it.

-Question (YM): What is the difference between Temporary Data Library and Permanent Data Library?
-Answer (YM): If not library name is specified, SAS by defaults creates the data in temporary library called Work. However, this library doesn't persist when the SAS session is closed.

## Chapter 3 Questions
- Question (AS): Is there a way to print out the values of certain variables during debugging i.e. equivalent of a print statement?
- Answer: TBD

- Question (YM): What are three different types of Programming Windows in SAS application? Describe.
- Answer (YM): SAS has three different types of Windows, Editor Window, Log Window and Output Window. Log window is where all SAS code is created and edited. All SAS files by default are opened with this window. Log window is where all Errors and Warning are written during the session for DATA and PROC steps. Output windows are where all the reports and output are generated. 

Question (YM): What happens if a SAS statement is not terminated with a semicolon?
Answer(YM): If the statement is not terminated with a semicolon, SAS considers the next statement as part of the original statement and SAS will generate a error message whichi most likely will be a syntax error.


## Chapter 4 Questions
[Chapter 4, Problem 10]
- Question(BP): Can PROC PRINT default be changed for a session?
- Answer(BP):DATA and PROC statements signal the beginning of a new step. When SAS encounters a subsequent DATA, PROC, or RUN statement (for DATA steps and most procedures) or a QUIT statement (for some procedures), SAS stops reading statements and executes the previous step in the program. In our sample program, each step ends with a RUN statement.
- Question(BP): Does Data step statement produces output after executing Data step statement?
- Answer(BP) When the program is processed, it creates the SAS data set. The DATA step produces messages in the SAS log, but it does not create a report or other output.
- Question (YM): What is the basic form of report in SAS and how can it be produced?
- Answer (YM): The most basic report can be created using PROC statement PROC PRINT DATA=Data_Source; RUN; This is similar to doing a select * from table_name statement in SQL.
- Question (YM): What happens when OUT= option is not specified in PROC statement PROC SORT?
- If not OUT= option is provided, PROC SORT will overwrite the original dataset with the sorted results.

## Chapter 5 Questions
[Chapter 5, Problem 7]
- Question (AS): How to read a raw data set in which each observation's data values are on two lines?
- Answer (AS): SAS provides the slash (/) and #n to handle cases where more than one record in the input file is required to compose one observation in the dataset. When SAS encounters a slash, it continues to read values till end of Input statement. Then writes the PDV out as one observation. The slash is a relative line pointer and #n is a specifc line pointer.
- Question (SK): Is there a way we can change the columns name and its size once we defined them ? How can we delete a column or reduce its size?
- Answer: TBD
- Question (YM): What happens to excel data that is imported in SAS if excel file has different sheets?
- Answer (YM): If more than one sheets are there in an excel sheet, they are made available in SAS library as different datasets.


## Chapter 6 Questions
[Chapter 6, Problem 3]
- Question (AS): What are the additional commands used to direct the DATA step not to execute for each record? What are the conditions in which we need to use such commands and what are the advantages? Can we give an example?
- Answer (AS): Each iteration of a data step reads in data from the input file into the buffer,  the input statement writes it into the program data vector, and  at the end of the DATA step,SAS writes teh PDV contents out into the result dataset. Sometimes, you may need to test some conditions for selecting what observations get written out into teh result dataset. Based on an IF condition, The DELETE statement can be used to stop processing current iteration of data step and return to the beginning of the data step so that teh row is not written out to the result dataset.   
- Question (YM): What errors are detected during compilation phase and execution phase?
- Answer (YM): TBD
- Question (YM): How is a PUT statement useful in SAS programs?
- PUT statement can be used to print custom messages in the log file inside a PROC or DATA step. It is very useful to print custom messages,and printing variable values which can be very useful for debugging.

[Chapter 6 , Problem 6]
- Question (SK): When does LINES or CARDS  statements are used in the last statement of a data step ? when both are alias of   DATALINE statement?
- Answer (SK): TBD


## Chapter 7 Questions
- Question (YM): What is the difference between placing FORMAT in DATA step vs PROC step?
- Answer (YM): If FORMAT is placed in DATA step, it permanently associates that format with the variable where as in PROC step, the data is only displayed in that format.

## Chapter 8 Questions
- Question (YM) What are the different descriptive statistics produced by SAS?
- Answer (YM): The different descriptive statistics produced by SAS are confidence limit (CLM), Corrected sum of Squares (CSS), Coefficient of Variation (CV), Kurtosis (Kurtosis), LCLM (One sided confidence limit), Maximum (MAX), Average(MEAN), Mode (MODE), Minimum (MIN), N(Number of Obs), Num of Obs with missing values (NMISS), Range (RANGE), Skewness (SKEWNESS), Std Dev (STD), Standard error of mean (STDERR), sum(SUM), Sum of the weight variable values(SUMWGT), Uncorrected sum of squares (USS), Variance (VAR).

## Chapter 10 Questions
- Question (YM): Does proper indentation required in SAS?
- Answer (YM): Proper indentation is not required in SAS, however it's a good practice to have proper indentation so the code becomes easier to read and debug and loops and conditional statements can be easily identified where they are beginging and ending.


## Chapter 11 Questions
- Question (YM): What is the difference between specifying DROP= and KEEP= statemetns in DATA or SET statements?
- Answer (YM): Depening on where DROP= and KEEP= are specified, the data will be retained either in the output or input.

## Chapter 12 Questions

* **[Chapter 12, Problem 4]**
 * Question (JG): What is the result of submitting the following program?
 ```SAS
        data work.getobs5;
            obsnum=5;
            set company.usa(keep=manager payroll) point=obsnum;
            stop;
        run;
```

 * Answer: TBD
 
 - Question (YM): What is the difference between Merge and Append?
 - Answer (YM): Merge will combine data horizontally based on common variable values whereas append will add the data vertically. The difference is adding columns vs rows.
 
## Chapter 13 Questions
- Question (YM): What is the difference between PUT and INPUT?
- Answer (YM): TBD

## Chapter 14 Questions
- Question (YM): What are the different types of loops and condition statements supported by SAS?
- Answer (YM): TBD


## Chapter 15 Questions


## Chapter 16 Questions


## Chapter 17 Questions


## Chapter 19 Questions


## Chapter 20 Questions
