# JavaScript CodeWars Solutions

This the my repository for my codewars solutions in JavaScript.

## Problems
### 01 - Persistent Bugger (6 Kyu)
Write a function, persistence, that takes in a positive parameter num and returns its multiplicative persistence, which is the number of times you must multiply the digits in num until you reach a single digit.

For example:
```javascript
persistence(39) === 3 // because 3*9 = 27, 2*7 = 14, 1*4=4
                      // and 4 has only one digit

persistence(999) === 4 // because 9*9*9 = 729, 7*2*9 = 126,
                      // 1*2*6 = 12, and finally 1*2 = 2

persistence(4) === 0 // because 4 is already a one-digit number
```

### 02 - Ones and Zeros (7 kyu)
Given an array of one's and zero's convert the equivalent binary value to an integer.

Eg: [0, 0, 0, 1] is treated as 0001 which is the binary representation of 1
```javascript
Testing: [0, 0, 0, 1] ==> 1
Testing: [0, 0, 1, 0] ==> 2
Testing: [0, 1, 0, 1] ==> 5
Testing: [1, 0, 0, 1] ==> 9
Testing: [0, 0, 1, 0] ==> 2
Testing: [0, 1, 1, 0] ==> 6
Testing: [1, 1, 1, 1] ==> 15
Testing: [1, 0, 1, 1] ==> 11
```

### 03 - Printer Errors (7 kyu)
In a factory a printer prints labels for boxes. For one kind of boxes the printer has to use colors which, for the sake of simplicity, are named with letters from a to m.

The colors used by the printer are recorded in a control string. For example a "good" control string would be aaabbbbhaijjjm meaning that the printer used three times color a, four times color b, one time color h then one time color a...

Sometimes there are problems: lack of colors, technical malfunction and a "bad" control string is produced e.g. aaaxbbbbyyhwawiwjjjwwm.

You have to write a function printer_error which given a string will output the error rate of the printer as a string representing a rational whose numerator is the number of errors and the denominator the length of the control string. Don't reduce this fraction to a simpler expression.

The string has a length greater or equal to one and contains only letters from a to z.

Examples:
```javascript
s="aaabbbbhaijjjm"
error_printer(s) => "0/14"

s="aaaxbbbbyyhwawiwjjjwwm"
error_printer(s) => "8/22"
```

### 04 - Array.diff (6 kyu)
Your goal in this kata is to implement an difference function, which subtracts one list from another.

It should remove all values from list a, which are present in list b.
```javascript
array_diff([1,2],[1]) == [2]
```
If a value is present in b, all of its occurrences must be removed from the other:
```javascript
array_diff([1,2,2,2,3],[2]) == [1,3]
```

### 05 - A square of squares (8 kyu)
You like building blocks. You especially like building blocks that are squares. And what you even like more, is to arrange them into a square of square building blocks!

However, sometimes, you can't arrange them into a square. Instead, you end up with an ordinary rectangle! Those blasted things! If you just had a way to know, whether you're currently working in vain… Wait! That's it! You just have to check if your number of building blocks is a perfect square.

Task: Given an integral number, determine if it's a square number:

In mathematics, a square number or perfect square is an integer that is the square of an integer; in other words, it is the product of some integer with itself.
The tests will always use some integral number, so don't worry about that in dynamic typed languages.

Examples
```javascript
isSquare(-1) // => false
isSquare( 3) // => false
isSquare( 4) // => true
isSquare(25) // => true
isSquare(26) // => false
```

### 06 - Remove First and Last Character (8 kyu)
It's pretty straightforward. Your goal is to create a function that removes the first and last characters of a string. You're given one parameter, except in C, where, to keep the difficulty at the level of the kata, you are given two parameters, the first a buffer with length exactly the same as the second parameter, the original string. You don't have to worry with strings with less than two characters.


### 07 - Calculating with Functions (5 kyu)
This time we want to write calculations using functions and get the results. Let's have a look at some examples:
```javascript
seven(times(five())); // must return 35
four(plus(nine())); // must return 13
eight(minus(three())); // must return 5
six(dividedBy(two())); // must return 3
```
Requirements:

* There must be a function for each number from 0 ("zero") to 9 ("nine")
* There must be a function for each of the following mathematical operations: plus, minus, times, dividedBy (divided_by in Ruby)
* Each calculation consist of exactly one operation and two numbers
* The most outer function represents the left operand, the most inner function represents the right operand

### 08 - Descending Order (7 kyu)
Your task is to make a function that can take any non-negative integer as a argument and return it with its digits in descending order. Essentially, rearrange the digits to create the highest possible number.

Examples:
```javascript
Input: 21445 Output: 54421
Input: 145263 Output: 654321
Input: 1254859723 Output: 9875543221
```

### 09 - Find the smallest integer in the array (7 kyu)
Given an array of integers your solution should find the smallest integer.

For example:
```javascript
Given [34, 15, 88, 2] your solution will return 2
Given [34, -345, -1, 100] your solution will return -345
```
You can assume, for the purpose of this kata, that the supplied array will not be empty.