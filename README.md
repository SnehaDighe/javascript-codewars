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

### 10 - Find the odd int (7 kyu)
Given an array, find the int that appears an odd number of times. There will always be only one integer that appears an odd number of times.

### 11 - Find the next perfect square (7 kyu)
You might know some pretty large perfect squares. But what about the NEXT one?

Complete the findNextSquare method that finds the next integral perfect square after the one passed as a parameter. Recall that an integral perfect square is an integer n such that sqrt(n) is also an integer.

If the parameter is itself not a perfect square, than -1 should be returned. You may assume the parameter is positive.

Examples:
```javascript
findNextSquare(121) --> returns 144
findNextSquare(625) --> returns 676
findNextSquare(114) --> returns -1 since 114 is not a perfect
```

### 12 - Duplicate Encoder (6 kyu)
The goal of this exercise is to convert a string to a new string where each character in the new string is '(' if that character appears only once in the original string, or ')' if that character appears more than once in the original string. Ignore capitalization when determining if a character is a duplicate.

Examples:
```javascript
"din" => "((("

"recede" => "()()()"

"Success" => ")())())"

"(( @" => "))(("
```

### 13 - Simple Encryption #1 - Alternating Split (6 kyu)
For building the encrypted string: Take every 2nd char from the string, then the other chars, that are not every 2nd char, and concat them as new String. Do this n times!

Examples:
```javascript
"This is a test!", 1 -> "hsi  etTi sats!"
"This is a test!", 2 -> "hsi  etTi sats!" -> "s eT ashi tist!"
```
Write two methods:
```javascript
function encrypt(text, n)
function decrypt(encryptedText, n)
```
For both methods:   
If the input-string is null or empty return exactly this value!   
If n is <= 0 then return the input text.

### 14 - Tribonacci Sequence (6 kyu)
Well met with Fibonacci bigger brother, AKA Tribonacci.

As the name may already reveal, it works basically like a Fibonacci, but summing the last 3 (instead of 2) numbers of the sequence to generate the next. And, worse part of it, regrettably I won't get to hear non-native Italian speakers trying to pronounce it :(

So, if we are to start our Tribonacci sequence with `[1, 1, 1]` as a starting input (AKA signature), we have this sequence:
```javascript
[1, 1 ,1, 3, 5, 9, 17, 31, ...]
```
But what if we started with `[0, 0, 1]` as a signature? As starting with `[0, 1]` instead of `[1, 1]` basically shifts the common Fibonacci sequence by once place, you may be tempted to think that we would get the same sequence shifted by 2 places, but that is not the case and we would get:
```javascript
[0, 0, 1, 1, 2, 4, 7, 13, 24, ...]
```
Well, you may have guessed it by now, but to be clear: you need to create a fibonacci function that given a signature array/list, returns the first n elements - signature included of the so seeded sequence.

Signature will always contain 3 numbers; n will always be a non-negative number; if `n == 0`, then return an empty array and be ready for anything else which is not clearly specified ;)

### 15 - Rot13 (5 kyu)
ROT13 is a simple letter substitution cipher that replaces a letter with the letter 13 letters after it in the alphabet. ROT13 is an example of the Caesar cipher.
    
Create a function that takes a string and returns the string ciphered with Rot13. If there are numbers or special characters included in the string, they should be returned as they are. Only letters from the latin/english alphabet should be shifted, like in the original Rot13 "implementation".

### 16 - IPv4 to int32 (6 kyu)
Take the following IPv4 address: 128.32.10.1 This address has 4 octets where each octet is a single byte (or 8 bits).
    
* 1st octet 128 has the binary representation: 10000000
* 2nd octet 32 has the binary representation: 00100000
* 3rd octet 10 has the binary representation: 00001010
* 4th octet 1 has the binary representation: 00000001

So 128.32.10.1 == 10000000.00100000.00001010.00000001

Because the above IP address has 32 bits, we can represent it as the 32 bit number: 2149583361.

Write a function ip_to_int32(ip) ( JS: `ipToInt32(ip)` ) that takes an IPv4 address and returns a 32 bit number.
```javascript
ipToInt32("128.32.10.1") => 2149583361
```

### 17 - Write Number in Expanded Form (6 kyu)
You will be given a number and you will need to return it as a string in Expanded Form. For example:
```javascript
expandedForm(12); // Should return '10 + 2'
expandedForm(42); // Should return '40 + 2'
expandedForm(70304); // Should return '70000 + 300 + 4'
```
NOTE: All numbers will be whole numbers greater than 0.


### 18 - If you can read this... (6 kyu)
If you can read this...
The idea for this Kata came from 9gag today.here

You'll have to translate a string to Pilot's alphabet (NATO phonetic alphabet) wiki.

Like this:

`Input:` If you can read    
`Output:` India Foxtrot Yankee Oscar Uniform Charlie Alfa November Romeo Echo Alfa Delta

### 19 - Multiplication Tables  (6 kyu)
Create a function that accepts dimensions, of Rows x Columns, as parameters in order to create a multiplication table sized according to the given dimensions. **The return value of the function must be an array, and the numbers must be Fixnums, NOT strings.

Example:
```javascript
multiplication_table(3,3)

1 2 3
2 4 6
3 6 9

-->[[1,2,3],[2,4,6],[3,6,9]]
```
Each value on the table should be equal to the value of multiplying the number in its first row times the number in its first column.


### 20 - Function Cache (5 kyu)
If you are calculating complex things or execute time-consuming API calls, you sometimes want to cache the results. In this case we want you to create a function wrapper, which takes a function and caches its results depending on the arguments, that were applied to the function.
    
Usage example:
```javascript
var complexFunction = function(arg1, arg2) { /* complex calculation in here */ };
var cachedFunction = cache(complexFunction);

cachedFunction('foo', 'bar'); // complex function should be executed
cachedFunction('foo', 'bar'); // complex function should not be invoked again, instead the cached result should be returned
cachedFunction('foo', 'baz'); // should be executed, because the method wasn't invoked before with these arguments
```