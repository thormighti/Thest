# Thest

# Test

## Introduction
- You are **required** to use the .NET Framework, using either .NET Core or .NET 4.5 or above.
- You are **expected** to use NuGet packages.
- You are **required** to create a local git repository.
- You are **required** to commit **at least once at then end of each step** (you **may** create as many intermediaries as you wish, but **must** clearly indicate which commits are the final version for each step).

## Evalutation methods and critera
  - Each step will be reviewed separately. Do not skip any steps. Make your commits clear so we can easily find the final version of each step.
  - You will be evaluated on your solutions:
  - code beauty (easy to read and understand),
  - efficiency (power, memory consumption, etc.),
  - sturdiness,
  - extensibility,
  - testing methods and coverage.

## Before your start
- Some formulations in the specification are vague and generic on purpose. There is no 'perfect' or 'single' solution. We expect you to be able to explain and justify your choices if asked.
- We expect you to spend a "few hours" on the test. If you cannot complete in a reasonable time (from your appreciation), you can still send what you have achieved. Perhaps it's a good start.
- Feel free to cut out parts of the specs as long as you are confident enough in the way to implement it in your architecture and it feels redundant with another part. We'll ask you about the missing parts.

### Read the instructions again, take a break . . . and . . . Go !

## Part 1 - Console

### Step 1

Create a console application that reads a big CSV file (available [here](https://beezupcdn.blob.core.windows.net/recruitment/bigfile.csv "bigfile.csv")).
For each row where the sum of the integer value of ColumnC and the integer value of ColumnD is greater than 100, print out the concatenation of ColumnA & ColumnB.
Rows that can't be processed corretly should by skipped.

### Step 2

Replace the output from the previous step. Write a big JSON array of objects for the previous matched lines:
- Rows that can be processed correctly with C + D > 100: { "lineNumber": <FILE_LINE_NUMBER>, "type": "ok", "concatAB": "<PREVIOUS_AB_CONCAT>", "sumCD": <PREVIOUS_CD_SUM> }
- Rows that can't be processed correctly : { "lineNumber": <FILE_LINE_NUMBER>, "type": "error", "errorMessage": <ERROR_MESSAGE> }

### Step 3

Output format (plain text, JSON, etc.) can now be configured by command line arguments. Integrate at least one new format.

## Part 2 - API

### Step 1

Creat an API prject that can receive HTTP POST and GET requests on /filter?csvUri={<CSV_URI>}.
The payload response should be a json object as described in Part1

### Step 2

This API should be able to ouput Text, Json, CSV, XML ... 
Update the API to be able to return JSON or XML formats for the payload response.

## Final (this step should be the easy one)

We are constantly trying to improve our test. Any constructive fedback (too long, too easy, too vague, missing parts, you wanted to show something else ...) on this test is welcome.
