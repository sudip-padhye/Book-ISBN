# Book-ISBN (ISBN Verifier & Generator)

## Problem Statement:
An ISBN (International Standard Book Number) is a ten digit code that uniquely identifies a book. The first 9 digits are used to represent the book and the 10th digit is used to ensure that the ISBN is correct. To validate the ISBN number, calculate a sum that is 10 times the first digit plus 9 times the second digit plus 8 times the third digit ... all the way until you add 1 times the last digit. If the sum is divisible by 11, then the 10 digit code is a valid ISBN number. 

For example 1111456291 is a valid ISBN, because

10*1 + 9*1 + 8*1 + 7*1 + 6*4 + 5*5 + 4*6 + 3*2 + 2*9 + 1*1 = 132 which is divisible by 11.

Each of the first nine digits can take a value between 0 and 9. Sometimes it is necessary to make the last digit equal to ten. This is done by writing the last digit as X.
For example, 156881111X is a valid ISBN, because
10*1 + 9*5 + 8*6 + 7*8 + 6*8 + 5*1 + 4*1 + 3*1 + 2*1 + 1*10 = 231 which is divisible by 11.

You have to write a program to fill in the missing digit from a given ISBN number where the missing digit is represented as '?'. The missing digit should be a value between 0 and 9 or 'X' (X represents 10)

## Working
The program has 3 options -
•	Validate ISBN
•	Determine the missing character
•	Generate an ISBN

### 1.Validate ISBN-

Takes an ISBN as input and checks for its validity.
Eg-
1. Enter Book ISBN:1245631789X
   Invalid ISBN

2. Enter Book ISBN:6546873850
   Valid ISBN

### 2.Determine the missing character-

Fetches a missing character in the given ISBN. The missing character is displayed using "?" mark.
Input Format
Line 1	A single line with a ten digit ISBN number that contains '?' in a single position. The length of the input should be 10 characters.
 
Output Format
•         The output should contain the missing digit.
•         The length of the output field defined in the program should be 1.
•         If a suitable value for '?' cannot be found which makes the ISBN valid, then the text 'NO SOLUTION POSSIBLE' should be displayed as output.
 
### 3.Generate an ISBN-
Generates a random valid ISBN using rand( ) function. During generation, the first 9 digits are generated randomly and then to make it divisible by 11, the last character is assigned in the range 0-X.
Eg-
1.The generated ISBN is:8345957684
2.The generated ISBN is:7462653532
