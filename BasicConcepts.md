# Basic Concepts

- Bits/Bytes: Understanding the basic unit of information storage and manipulation in a computer system.
- Variables: Named storage locations used to hold values that can be modified during program execution.
- Data Types: The different kinds of data that can be stored in variables, such as numbers, characters, booleans, etc.
- Conditional Statements:

  - If-else: Allows the program to make decisions based on a condition.
  - Switch: Provides multiple branches of execution based on different values of a variable.

- Loops:

  - While: Repeatedly executes a block of code while a condition is true.
  - For: Repeats a block of code a specific number of times.
  - Do-while: Executes a block of code at least once, then repeatedly executes it while a condition is true.

- Operators:

  - Arithmetic Operators:

    - Addition (+)
    - Subtraction (-)
    - Multiplication (\*)
    - Division (/)
    - Modulo (Remainder) (%)

  - Assignment Operators:

    - Assignment (=)
    - Compound assignment operators (e.g., +=, -=, \*=, /=)

  - Comparison Operators:

    - Equal to (==)
    - Not equal to (!=)
    - Greater than (>)
    - Less than (<)
    - Greater than or equal to (>=)
    - Less than or equal to (<=)

  - Logical Operators:

    - Logical AND (&&)
    - Logical OR (||)
    - Logical NOT (!)

  - Increment/Decrement Operators:

    - Increment (++)
    - Decrement (--)

- Scope
- Functions/Methods: Blocks of reusable code that perform specific tasks and can be called from different parts of the program.
- Arrays/Lists: Data structures that allow storing multiple values in a single variable, enabling efficient storage and retrieval of data.
- Advanced structures: Dictionaries, Sets, ...

## Bits / bytes

- a bit is either a 1 or 0;
- 1 byte is 8 zeroes or ones;
- 8 bits are 1 byte;
- Respresents the amount of space on a computer.
- Bits are the building blocks of all digital information.

-> **what's inside the box (anything can be represented as 0's and 1's if you have enough of them)**

## Variables

Variables are things (a place in your computer memory) you can temporarily store things (you can move things, you delete things, you can change, it can be damaged, anything, Objects) in, to use them later and store them indefinitely.

-> **the box (something that points to whats inside, but used like this, so you can easily work with it)**

```bash
# representation of memory
# 1 byte, or 8 bits

[0][1][0][1][1][0][1][0]

# structure of a variable (nearly always)
# something (can be any name, since its just a name that points to information on your computer) equals something-else (can be anything)
something = ""
```

example:

```javascript
let hey = "text only";
```

```ruby
something = ""
```

```java
String blabla = "";
```

---

## Types

In most programming languages:

1. Object (umbrella, everything is an object);
2. String (text, made up of characters, or a list of characters);
3. Char (character);
4. Number;
5. Boolean (a bit, either 0 or 1, true or false, 1 is equal to one 1? -> yes: true, the earth is flat? -> no, false);

Example of a type:
Picture, Video, String

-> **Label on the box (tells you what you can expect inside of the box)**

## If else

### Definition

An if-else block (always together), is something that happens conditionally.

### Structure

```ruby
if (condition) then
    # ...
else
    # ...
end
```

### Examples

#### ruby

```ruby
you = "happy";

## only if else
# if (you == "happy") then
#     smile()
# else
#     cry()
# end

## include elseif
# if (you == "happy") then
#     smile()
# elsif (you == "angry")
#     frown()
# else
#     cry()
# end

## if else in if else
# if (you == "happy") then
#     smile()
# elsif (you == "angry")
#     you = "hungry"

#     if(you == "hungry") then
#         frown() && eat()
#     else
#         punchWall()
#     end
# else
#     cry()
# end

## multiple if conditions
if (you == "happy") then
    smile()
elsif (you == "angry" && you == "hungry") then
    frown()
    eat()
elsif (you == "angry")
    frown()
elsif (you == "hungry") then
    eat()
else
    cry()
    punchWall()
end

## switch case
case you
when "happy"
  smile()
when "angry" && "hungry"
  frown()
  eat()
when "angry"
  frown()
when "hungry"
  eat()
else
  cry()
  punchWall()
end
```

#### Javascript

```javascript
if (you == "happy") {
  smile();
} else if (you == "angry" && you == "hungry") {
  frown();
  eat();
} else if (you == "hungry") {
  eat();
} else if (you == "angry") {
  frown();
} else {
  cry();
  punchWall();
}

switch (you) {
  case "happy":
    smile();
    break;
  case "angry":
    frown();
    break;
  case "hungry":
    eat();
    break;
  default:
    cry();
    punchWall();
    break;
}
```

#### Java

```java
if (you == "happy"){
    smile()
}
else if (you == "angry" && you == "hungry") {
    frown()
    eat()
}
else if (you == "hungry") {
    eat()
}
else if (you == "angry"){
    frown()
}
else {
    cry()
    punchWall()
}

switch (you) {
    case "happy":
        smile();
        break;
    case "angry":
        frown();
        break;
    case "hungry":
        eat();
        break;
    default:
        cry();
        punchWall();
        break;
}
```

## Loops

### Why use loops?

In order to not repeat yourself thousands, or even millions, or even hundereds of times, we use loops, to say as long as a condition is true do what's inside of the loop.

```ruby
# You don't want this shit.
# its long and ugly and annoying to work with, imagine reading million lines of code like this. Dead dead dead!
smile()
smile()
smile()
smile()
cry()
cry()
punchWall()
punchWall()
punchWall()
punchWall()
smile()
smile()
smile()
smile()
cry()
cry()
punchWall()
punchWall()
punchWall()
punchWall()
```

```ruby
# You want this shit.
# concise, to the point and works in a smart way, things you want to happen all the time, happen ez clap
while (you == "alive") do
    while (you == "happy") do
        smile()
    end
    while (you == "sad") do
        cry()
    end
    while (you == "angry") do
        punchWall()
    end
end
```

### While

#### while Definition

As long as the condition is met, do something.

#### while Syntax

```ruby
while (true) do
    something()
end
```

### For

#### for Defintion

X amount of times, do something.

#### for Syntax

```ruby
for counter in 0..100 do
    something()
end

# show the numbers from 0 to 100
for counter in 0..100 do
    puts(counter)
end

# example of for as a while
counter = 0
while (counter <= 100) do
    puts(counter)
    # first time 0
    # second time 1
    counter = counter + 1
    # first time its 0 + 1 = 1
    # second time its 1 + 1 = 2
end
```

```javascript
const array = [1, 2, 3, 4];

for (let counter = 0; counter < array.length; counter++) {
  console.log(array[counter]);
  // 1
  // 2
  // 3
  // 4
  // NaN
}
```

### Do while

#### do while Defintion

Exactly the same as a while, except it happens at least once.

#### do while Syntax

```javascript
let x = -1;

do {
  print(x);
  // show -1
} while (x > 10);

// code above instead with while
let x = -1;

print(x);
while (x > 10) {
  print(x);
}
```

## Scope

### What is scope?

Some created variables have a different scope, depending on identifier.

In JS, you have 3 ways to create a variable:

- `let`: local scope
- `const`: local scope
- `var`: global scope

### Var -- deprecated (a.k.a. NEVER EVER FUCKING USE IT)

`var` is different from `let` and `const`, in the way that when you create a `var` variable that's its declared in the whole document.
Which means in other words, no matter where you are in a function, outside of a function, somewhere else, that you can access the `var` variable, e.g.:

```javascript
// Example using var
function exampleVar() {
  if (true) {
    var x = 10;
    console.log(x); // Output: 10
  }
  console.log(x); // Output: 10
  x = 20;
  console.log(x); // Output: 20
}
exampleVar();
console.log(x); // Output: ReferenceError: x is not defined
```

As seen in the example, even when you create a variable with `var` in an if-block, you can still access it outside of the if-block.
This can lead to some unexpected behaviour... and is generally bad practice.

### Let and const

With `let` and `const` variables are restricted to the local-scope. It's only accessible in the block that it is declared and underlying blocks.
Which means that you can't access a variable outside of where it is declared (e.g.: if/for/while/...).

Example of `let`:

```javascript
// Example using let
function exampleLet() {
  if (true) {
    let y = 10;
    console.log(y); // Output: 10
  }
  console.log(y); // Output: ReferenceError: y is not defined
  y = 20;
  console.log(y); // Output: 20
}
exampleLet();
console.log(y); // Output: ReferenceError: y is not defined
```

Example of `const`:

```javascript
// Example using const
function exampleConst() {
  if (true) {
    const z = 10;
    console.log(z); // Output: 10
  }
  console.log(z); // Output: ReferenceError: z is not defined
  z = 20; // Error: Assignment to constant variable.
}
exampleConst();
console.log(z); // Output: ReferenceError: z is not defined
```

## Functions and Methods

### Functions

#### Functions definition

Methods / fuctions are used, to avoid writing the same code multiple times. Imagine a world, in which you didn't have methods or functions, you would have to write certain parts 1000x over and over again, just as with loops. But if you ever had to make a (small / big) change in code, that is written 1000x and practically the same, you would have to do it everywhere. If the change only took 1 second, you would already lose 1000 seconds or 15 minutes.
Modulo

#### method SyntaxAddition (+)

- Subtraction (-)
- Multiplication (\*)
- Division (/)
- Modulo (Remainder) (%)

```ruby

# lambda

(a) -> a\*\*2

```

#### Examples of methods

```javascript
function celsius(a) {
  console.log(a * 2 + 30);
}

// lambda
// const celsius = (a) => console.log(a * 2 + 30);

celsius(77);
celsius(88);
```

```java
Public Class Methods {
    Public static void main (string[] args) {
        int a = 4;
        int b = 3;
        systme.out.println(a * b);

        int c = 8;
        int d = 34;
        systme.out.println(c * d);

        int e = 67;
        int f = 90;
        systme.out.println(e * f);
    }
}
```

```Java
Public Class Methods {
    Public static void main (string[] args) {
        Multiply(4, 3);
        Multiply(8, 34);
        Multiply(67, 90);
        Multiply(75, 4);
    }
     Public static void multiply (int a, int b) {
        System.out.println(a * b)
    }
}
```

## Operators

### Arithmetic Operators

#### Addition (+)

```javascript
function three() {
  return 3;
}

function four() {
  return 4;
}

console.log(three() + four());
// 7
```

#### Subtraction (-)

```javascript
function three() {
  return 3;
}

function four() {
  return 4;
}

console.log(three() - four()); // -1
```

#### Multiplication (\*)

```javascript
function three() {
  return 3;
}

function four() {
  return 4;
}

console.log(three() * four()); // 12
```

#### Division (/)

```javascript
function three() {
  return 3;
}

function four() {
  return 4;
}

console.log(three() / four()); // 0.75
```

#### Modulo (Remainder) (%)

```javascript
function three() {
  return 3;
}

function four() {
  return 4;
}

console.log(three() % four()); // 3
```

### Assignment Operators

#### Assignment (=)

```ruby
three = 3
print(three) # 3
three = 10
print(three) # 10
```

#### Compound assignment operators (e.g., +=, -=, \*=, /=, %=)

```javascript
let three = 3;
print(three); // 3

three += 3;
// the same as: three = three + 3
print(three); // 6

three -= 3;
// the same as: three = three - 3
print(three); // 3

three *= 3;
// the same as: three = three * 3
print(three); // 9

three /= 3;
// the same as: three = three / 3
print(three); // 3

three %= 3;
// the same as: three = three % 3
print(three); // 0
```

### Comparison Operators

#### Equal to (==)

Check the equality between 2 items. Is 1 equal to 1? yes, then it returns true. Is 2 equal to 4? no, then it returns false.

```ruby
three = 3
print(three == 3) # true
print(three == 4) # false
print(true == true) # true
print(false == true) # false
```

#### Not equal to (!=)

```ruby
three = 3
print(three != 3) # false
print(three != 4) # true
print(true != true) # false
print(false != true) # true
```

#### Greater than (>)

```ruby
three = 3
print(three > 3) # false
print(three > 4) # false
print(three > 0) # true
```

#### Less than (<)

```ruby
three = 3
print(three < 3) # false
print(three < 4) # true
print(three < 0) # false
```

#### Greater than or equal to (>=)

```ruby
three = 3
print(three >= 3) # true
print(three >= 4) # false
print(three >= 0) # true
```

#### Less than or equal to (<=)

```ruby
three = 3
print(three <= 3) # true
print(three <= 4) # true
print(three <= 0) # false
```

### Logical Operators

#### Logical AND (&&)

```ruby
three = 3
iAmBeautiful = true
# && meaning that if one of the velue is true and others are false then the result will be false
print(three <= 3 && iAmBeautiful && 1 >= 0) # true
print(three <= 3 && iAmBeautiful && 1 <= 0) # false
print(three <= 4 && iAmBeautiful && 1 >= 0) # true
print(three <= 0 && iAmBeautiful && 1 >= 0) # false
```

#### Logical OR (||)

```ruby
three = 3
iAmBeautiful = true
# || menaing that if one of the value is true then the result will be true.
print(three <= 3 || iAmBeautiful || 1 >= 0) # true
print(three <= 3 || iAmBeautiful || 1 <= 0) # true
print(three <= 4 || iAmBeautiful || 1 >= 0) # true
print(three <= 0 || iAmBeautiful || 1 >= 0) # true
```

#### Logical NOT (!)

```ruby
three = 3
iAmBeautiful = true

print(!iAmBeautiful) # false
print(iAmBeautiful) # true
print(!(three == 3)) # false
print(!(three < 3)) # true
print(!(three > 3)) # true
print(!(three != 3)) # true
```

### Increment/Decrement Operators

#### Increment (++)

```javascript
let three = 3;

print(three); // 3

three++;
print(three); // 4

three += 1;
print(three); // 5

three++;
print(three); // 6
```

#### Decrement (--)

```javascript
let three = 3;

print(three); // 3

three--;
print(three); // 2

three -= 1;
print(three); // 1

three--;
print(three); // 0
```

## Arrays/lists

### Syntax

#### Array

First element starts at index 0.
Has a fixed length. Limited lists.

#### List

First element starts at index 0.
Has variable size.

#### Similarities

```ruby
beautifulList = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
userList = [user1, user2, user3, user4, user5, user6, user7, user8, user9, user10]

## array example
# array of size 4
# add 1 to array
# [1]
#
# array of size 4
# add 2 to array
# [1, 2]
#
# array of size 4
# add 3 to array
# [1, 2 , 3]
#
# array of size 4
# add 4 to array
# [1, 2, 3, 4]
# full
#
# array of size 4
# add 5 to array
# error


## list example
# list of size 4
# add 1 to list
# [1]
#
# list of size 4
# add 2 to list
# [1, 2]
#
# list of size 4
# add 3 to list
# [1, 2 , 3]
#
# list of size 4
# add 4 to list
# [1, 2, 3, 4]
# full
#
# try to add 5 to list
# size of list exceeded, make new array (under the hood), with double the size
# list of size 8
#  opy all items to the new array
# add 5 to list
# [1, 2, 3, 4, 5]
```

## Advanced Structures

### Map/Dictionaries

In real life:
A dictionary contains words with their explanation(-s).

In programming land:
A dictionary contains key-value pairs.
The key is the word, the value is the explanation or list of explanations.

```javascript
let cuteMappy = new Map();
cuteMappy.add(
  "smile",
  "a smile is an indication of happiness, but not exclusive to happiness alone, a smile can mean many things, but in general is associated with a happy and healthy person."
);
// key value pairs
```

### Set

A set is a list of unique values.
NO MULTIPLE THE SAME VALUES ALLOWED!

```javascript
let omgSettie = new Set();

omgSettie.add([
  1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 1, 2, 3, 4, 5, 6, 7, 8, 1, 2, 3, 1, 2, 3, 4, 5,
  6,
]);

print(omgSettie);
// [1, 2, 3, 4, 5, 6, 7, 8 , 9, 10]
```

## Exercises

### Calculate average of list of numbers

2 ways to do it:

1. calculate sum and then divide by amount of numbers.
2. add the division of number by amount to a variable called average.

```javascript
// first way
array = [1, 2, 3, 4];
sum += 1;
sum += 2;
sum += 3;
sum += 4;
// sum is 10

sum /=
  array.length[
    // sum is 10/4 =  2.5

    // second way
    (1, 2, 3, 4)
  ];
sum += 1 / array.length; // 0.25
sum += 2 / array.length; // 0.5
sum += 3 / array.length; // 0.75
sum += 4 / array.length; // 1
// sum = 2.5
```

#### Solution

```javascript
function findAverage(array) {
  // If there are "n" numbers in a list
  // then you divide the sum of the list with "n"
  // otherwise the result will be 0
  let average = 0;

  if (array.length > 0) {
    let sum = 0;

    for (let counter = 0; counter < array.length; counter++) {
      sum += array[counter];
    }

    average = sum / array.length;
  }

  return average;
}
```

### Calculate 0 to n, powers of 2

```javascript
function powersOfTwo(n) {
  // 2^n
  // n needs to be count from 0 inclusively
  // calculate for each number 2 to the power of the number x
  let calculatePowersOfTwo = [];
  for (let counter = 0; counter <= n; counter++) {
    let poweroftwo = 2 ** counter;
    calculatePowersOfTwo.push(poweroftwo); // to put it in the array
    console.log(poweroftwo);
  }

  return calculatePowersOfTwo;
}
```

### Sum of positive numbers

```javascript
function positiveSum(arr) {
  // you need to sum the positive numbers only
  // excude the negative numbers
  // then if you don't have any positive numbers then the sum is 0

  let sum = 0;

  for (let counter = 0; counter < arr.length; counter++) {
    if (arr[counter] > 0) {
      sum += arr[counter];
    }
  }
  return sum;
}
```

### Remove duplicates from lists (array)

```javascript
function distinct(a) {
  // removes duplicates/ only show a number once

  let noduplicates = new Set(a);
  let array = Array.from(noduplicates);

  return array;
}
```

### Returning Strings

```javascript
function greet(name) {
  // return a sentence differnetly input different words
  // "Hello, x how are you doing today?"
  let thegreeting = "Hello, " + name + " how are you doing today?";

  return thegreeting;
}
```

### Opposite number

#### example 1

```javascript
function opposite(number) {
  return number * -1;
}
```

#### example 2

```javascript
function opposite(number) {
  return -number;
}
```

### Is it a palindrome?

```javascript
function isPalindrome(x) {
  let y = "";
  x = x.toLowerCase(); // change from big letter to small letter.

  for (let counter = x.length - 1; counter >= 0; counter--) {
    y += x[counter]; // if you do 'y = x[counter]' then it replace every next letter everything so you will only get the last/first letter.
    console.log(y);
  }

  return y == x;
}
```

### Even or Odd?

```javascript
function evenOrOdd(number) {
  // number % 2 => if result 1 or -1 is odd, result 0 is even.
  let result = number % 2;
  // can't put result == 1|| -1 but you can put them separately tho.
  if (result == 0) {
    return "Even";
  } else {
    return "Odd";
  }
}
```

### Highest and Lowest

```javascript
function highAndLow(numbers) {
  // so return the highest number and the lowest number in the array or list
  // if you can't go above x number meaning the highest
  // if you can't go below x number meaning the lowest

  numbers = numbers.split(" ").map((i) => +i);
  let highest = numbers[0];
  let lowest = numbers[0];

  for (let counter = 1; counter < numbers.length; counter++) {
    let currentNumber = numbers[counter];

    if (currentNumber > highest) {
      highest = currentNumber;
    }
    if (currentNumber < lowest) {
      lowest = currentNumber;
    }
  }

  return highest + " " + lowest;
}
```

### Multiply

This code does not execute properly. Try to figure out why.

```javascript
function multiply(a, b) {
  return a * b;
}
```

### Convert boolean values to strings 'Yes' or 'No'

Complete the method that takes a boolean value and return a "Yes" string for true, or a "No" string for false.

```javascript
function boolToWord(bool) {
  if (bool == true) return "Yes";
  if (bool == false) return "No";
}
```

### Square(n) Sum

Complete the square sum function so that it squares each number passed into it and then sums the results together.
For example, for [1, 2, 2] it should return 9 because 12+22+22=91^2 + 2^2 + 2^2 = 912+22+22=

```javascript
function squareSum(numbers) {
  // first number * number each
  // then plus them together
  let sum = 0;
  for (let counter = 0; counter < numbers.length; counter++) {
    let squares = numbers[counter] * numbers[counter];
    sum += squares;
  }
  return sum;
}
```

### Return Negative

In this simple assignment you are given a number and have to make it negative. But maybe the number is already negative?

```javascript
function makeNegative(num) {
  if (num >= 0) {
    return -num;
  } // you don't need to add another if here because it already there and what you want to write next is the opposite of that if.
  // when you check for all numbers greater than or equal to 0, you don't have to check for number smaller than 0, since when you get that far, those numbers are the only numbers left, the other numbers got filtered out in the previous if statement
  return num;
}
```

### Reversed Strings

Complete the solution so that it reverses the string passed into it.
'world' => 'dlrow'

```javascript
function solution(str) {
  let reverse = ""; // you want reverse to be strings so you put that little two weird things

  for (let counter = str.length - 1; counter >= 0; counter--) {
    // the counter is set to length-1 because it start counting from 0 (the first letter is place 0)
    // the counter needs to be orderly 1 > 2 > 3
    reverse += str[counter];
  }

  return reverse;
}
```

### Convert a Number to a String

We need a function that can transform a number (integer) into a string. 123 --> "123"

```javascript
function numberToString(num) {
  return (num = "" + num); // =if you put "" it means that you want to turn the inside "" into words/ string.
  // or return ''+num
}
```

### Reversed sequence

Build a function that returns an array of integers from n to 1 where n>0.
Example : n=5 --> [5,4,3,2,1]

```javascript
const reverseSeq = (n) => {
  let reverse = []; // this is to create an array

  for (let counter = n; counter > 0; counter--) {
    reverse.push(counter); // this is yo put things in the array !!! can't use with stringd!!!
  }
  return reverse;
};
```

### Remove First and Last Character

```javascript
function removeChar(str) {
  let removezero = "";

  for (let counter = 1; counter < str.length - 1; counter++) {
    removezero += str[counter]; // if you want to reduce/increase the length of your array just usw - and  + sign with the number you want to reduce/increase
  }

  return removezero; // always return or console.log() to check your code! otherwise they might return "undefined"
}
```

### String repeat

Write a function that accepts an integer n and a string s as parameters, and returns a string of s repeated exactly n times.
6, "I" -> "IIIIII"

```javascript
function repeatStr(n, s) {
  let total = "";

  for (let counter = 0; counter < n; counter++) {
    total += s; // you don't need to put "counter" after "s",Since you put the "s" inside the "for" function, you don't have to repeat it. The counter is already there inside the "for" function.
  }
  return total;
}
```

### Contamination #1 -String

text before = "abc"
character = "z"
text after = "zzz"

```javascript
function contamination(text, char) {
  let result = "";

  for (let counter = 0; counter < text.length; counter++) {
    result += char;
  }
  return result;
}
```

### Grassshopper - sum

input 2, result 3 (1 + 2)
input 8, result 36 (1 + 2 + 3 + 4 + 5 + 6 + 7 + 8)

```javascript
var summation = function (num) {
  let total = 0;

  for (let counter = 0; counter < num + 1; counter++) {
    total += counter;
  }
  return total;
};
```

### Capitalization and Mutability

Make the first letter big (capitalized it)

```javascript
function capitalizeWord(word) {
  let followWords = "";
  let firstLetter = "";
  firstLetter = word[0].toUpperCase(); // capitalized words

  for (let counter = 1; counter < word.length; counter++) {
    followWords += word[counter];
  }
  return firstLetter + followWords;
}
```

### Multiple of index

They want you to return every number in the array, for which their index is X times (a multiple) the nunber at position index;

For instance, you receive the following array:
[1, 2, 3, 4, 5, 6, 7, 8, 12, 24]

your index starts of with 0 and there you have number 1, is 0+0+0+0 ever going to be 1? No

index 1, value 2, is 1+1+... ever going to be 2? Yes

```javascript
function multipleOfIndex(array) {
  let multiple = [];

  for (let counter = 0; counter < array.length; counter++) {
    if (array[counter] % counter == 0 || array[counter] == counter) {
      multiple.push(array[counter]);
    }
  }

  return multiple;
}
```

### Find the smallest integer in the array

Given [34, 15, 88, 2] your solution will return 2

```javascript
class SmallestIntegerFinder {
  findSmallestInt(args) {
    let smallest = args[0];

    for (let counter = 1; counter < args.length; counter++) {
      let number = args[counter];
      if (number < smallest) {
        smallest = number;
      } // this is a bit tricky, but if the number is < the smallest (the number position 0) then the smallest = number (which mean the smallest that we will be return is the number)
    }
    return smallest;
  }
}

// or return Math.min(...args); which ... is to take the number out of the array
```

### Remove String Spaces

Just remove the spaces between words

```javascript
function noSpace(x) {
  let text = "";

  for (let counter = 0; counter < x.length; counter++) {
    if (x[counter] != " ") {
      text += x[counter];
    }
  }
  return text;
}
// or return x.replaceAll(' ', '');
```

### Rounded to the smallest value

You get given the time in hours and you need to return the number of litres Nathan will drink, rounded to the smallest value.
he drinks 0.5 litres of water per hour of cycling.

```javascript
function litres(time) {
  let result = time * 0.5;
  result = Math.floor(result); // this use to round the number donw
  return result;
}
```

### Century from year

Given a year, return the century it is in.

```javascript
function century(year) {
  let century = year * 0.01;
  century = Math.ceil(century);

  return century;
}
```

### Basic Math

Examples(Operator, value1, value2) --> output
('+', 4, 7) --> 11
('-', 15, 18) --> -3

```javascript
function basicOp(operation, value1, value2) {
  let result = 0;
  if (operation == "+") {
    // == is to control if you put only = there, it means you conmand it.
    result = value1 + value2;
  } else if (operation == "-") {
    result = value1 - value2;
  } else if (operation == "*") {
    result = value1 * value2;
  } else if (operation == "/") {
    result = value1 / value2;
  } // "else" do not have conditions if you have conditions use "else if".
  return result;
}
```

Or

### Counting sheep

Only count true
For example,

[true, true, true, false,
true, true, true, true ,
true, false, true, false,
true, false, false, true ,
true, true, true, true ,
false, false, true, true]

The correct answer would be 17.

```javascript
function countSheeps(arrayOfSheep) {
  let presentSheep = 0;
  for (let counter = 0; counter < arrayOfSheep.length; counter++) {
    if (arrayOfSheep[counter] == true) {
      // if (arrayOfSheep[counter] != false && arrayOfSheep[counter] != null && arrayOfSheep[counter] != undefined){
      // presentSheep += arrayOfSheep[counter];
      // console.log(arrayOfSheep[counter])
      // console.log(presentSheep)
      presentSheep++;
    }
  }
  return presentSheep;
}
```

### Convert a String to a Number

```javascript
const stringToNumber = function (str) {
  return (str = str - "");
};
// return Number(str);
// return +str;
```

### Abbreviate a Two Word Name

The output should be two capital letters with a dot separating them.
It should look like this:
Sam Harris => S.H
patrick feeney => P.F

```javascript
function abbrevName(name) {
  let Firstletter = name[0];
  let Lastname = name.split(" ");

  return (Firstletter + "." + Lastname[1][0]).toUpperCase();
}
```

### Doubled values

Given an array of integers, return a new array with each value doubled.
For example:
[1, 2, 3] --> [2, 4, 6]

```javascript
function maps(x) {
  let result = [];
  for (let counter = 0; counter < x.length; counter++) {
    let calcu = x[counter] * 2;
    result.push(calcu);
  }
  return result;
}
// or  return x.map(n => n * 2);
```

### A Needle in the Haystack

Write a function findNeedle() that takes an array full of junk but containing one "needle"
After your function finds the needle it should return a message (as a string) that says:
"found the needle at position " plus the index it found the needle, so:

```javascript
function findNeedle(haystack) {
  for (let counter = 0; counter < haystack.length; counter++) {
    if (haystack[counter] == "needle") {
      return "found the needle at position " + counter;
    }
  }
}
```

### Is he gonna survive?

```javascript
function hero(bullets, dragons) {
  let result = bullets / 2;
  if (result >= dragons) {
    return true;
  } else {
    return false;
  }
}
```

### Convert number to reversed array of digits

```javascript
function digitize(n) {
  let reversedArray = [];
  n = n.toString();

  for (let counter = n.length - 1; counter >= 0; counter--) {
    reversedArray.push(Number(n[counter]));
  }

  return reversedArray;
}
```

### I love you, a little , a lot, passionately ... not at all

```javascript
// function howMuchILoveYou(nbPetals) {
//   switch (nbPetals) {
//     case 1:
//       return "I love you";
//     case 2:
//       return "a little";
//     case 3:
//       return "a lot";
//     case 4:
//       return "passionately";
//     case 5:
//       return "madly";
//     case 0:
//       return "not at all";
//     default:
//       return howMuchILoveYou(nbPetals-6)
//   }
// }

function howMuchILoveYou(nbPetals) {
  let rose = nbPetals % 6;

  switch (rose) {
    case 1:
      return "I love you";
      break;
    case 2:
      return "a little";
      break;
    case 3:
      return "a lot";
      break;
    case 4:
      return "passionately";
      break;
    case 5:
      return "madly";
      break;
    case 0:
      return "not at all";
      break;
  }
}
```

### plural

Is the number plural or not? such as 5 minutes, 14 apples, or 1 sun.

```javascript
function plural(n) {
  if (n == 1) return false;
  else return true;
}
// or return n !== 1;
```

### What's the real floor?

change from American floor system (1 2 3 4 5 6 ... 12 14 15 ...) to European floor system (0 1 2 3 4 5 6 ...)

```javascript
function getRealFloor(n) {
  // (n is) american floor [start with 1] => european floor [start with 0]
  // no floor 13 so if american floor 15 = european floor 13
  if (n >= 14) {
    return n - 2;
  } else if (n <= 0) {
    return n;
  } else {
    return n - 1;
  }
}
// or  if(n >= 13) return n - 2
//  if(n > 0) return n - 1
//  return n

// or return n > 13 ? n - 2 : n > 0 ? n - 1 : n;
```

### Opposites Attract

If one of the flowers == even and the other flowers == odd then that is "true" otherwise return false

```javascript
function lovefunc(flower1, flower2) {
  if (flower1 % 2 == 0 && flower2 % 2 == 1) {
    return true;
  } else if (flower2 % 2 == 0 && flower1 % 2 == 1) {
    return true;
  } else {
    return false;
  }
}
// or return flower1 % 2 !== flower2 % 2;
```

### Convert a Boolean to a String

```javascript
function booleanToString(b) {
  return b.toString();
}
```

### Get the Middle Character

You are going to be given a word. Your job is to return the middle character of the word. If the word's length is odd, return the middle character. If the word's length is even, return the middle 2 characters.

```javascript
function getMiddle(s) {
  let cal2 = s.length / 2;
  if (s.length % 2 == 0) {
    return s[cal2 - 1] + s[cal2];
  } else if (s.length % 2 == 1) {
    return s[Math.floor(cal2)];
  }
}
```

### vowel count

Return the number (count) of vowels in the given string.

We will consider a, e, i, o, u as vowels for this Kata (but not y).

The input string will only consist of lower case letters and/or spaces.

```javascript
function getCount(str) {
  let result = 0;
  for (let counter = 0; counter < str.length; counter++) {
    switch (str[counter]) {
      case "a":
      case "e":
      case "i":
      case "o":
      case "u":
        result++;
    }
  }
  return result;
}
```

### Drink about

Kids drink toddy.
Teens drink coke.
Young adults drink beer.
Adults drink whisky.

Make a function that receive age, and return what they drink.

Rules:

- Children under 14 old.
- Teens under 18 old.
- Young under 21 old.
- Adults have 21 or more.

```javascript
function peopleWithAgeDrink(old) {
  switch (true) {
    case old < 14:
      return "drink toddy";
    case old < 18:
      return "drink coke";
    case old < 21:
      return "drink beer";
    case old >= 21:
      return "drink whisky";
  }
}
```

### Squre numbers

Given an integral number, determine if it's a square number

```javascript
var isSquare = function (n) {
  let root = Math.ceil(n ** (1 / 2));
  if (root * root == n) {
    return true;
  } else {
    return false;
  }
};
```

### Is this a triangle?

Implement a function that accepts 3 integer values a, b, c. The function should return true if a triangle can be built with the sides of given length and false in any other case.

(In this case, all triangles must have surface greater than 0 to be accepted).

```javascript
function isTriangle(a, b, c) {
  // if a + b < c then it's not triagle
  [a, b, c] = [a, b, c].sort((a, b) => a - b);
  //a=[a,b,c].sort()[0]
  //b=[a,b,c].sort()[1]
  //c=[a,b,c].sort()[2]
  console.log(a, b, c);
  if (a + b <= c) {
    return false;
  } else if (a <= 0) {
    return false;
  } else if (b <= 0) {
    return false;
  } else if (c <= 0) {
    return false;
  } else {
    return true;
  }
}
```

### Exes and Ohs

Check to see if a string has the same amount of 'x's and 'o's. The method must return a boolean and be case insensitive. The string can contain any char.

```javascript
function XO(str) {
  str = str.toLowerCase();
  let x = 0;
  let o = 0;

  for (let counter = 0; counter < str.length; counter++) {
    if (str[counter] == "x") {
      x++;
    }
    if (str[counter] == "o") {
      o++;
    }
  }

  if (x == o) {
    return true;
  } else {
    return false;
  }
}
```


### Shortest Word

```javascript
function findShort(s) {
  s = s.split(" ");
  let firstword = s[0].length;
  for (let counter = 0; counter < s.length; counter++) {
    let currentwordlen = s[counter].length;
    if (currentwordlen < firstword) {
      firstword = currentwordlen;
    }
  }
  return firstword;
  // or  return Math.min(...s.split(" ").map((s) => s.length));
}
```

### Pythagorean Triple

```javascript
function isPythagoreanTriple(integers) {
  let [a, b, c] = integers.sort((a, b) => a - b);

  return a ** 2 + b ** 2 == c ** 2;
}
```

### Square Every Digit

```javascript
/*
 how does map work
 what tf is a join?
 do i still understand this code?
*/

function squareDigits(num){
  return Number(num.toString().split('').map((a) => a**2).join(''))
}
```

### Cat years, Dog years

```javascript
var humanYearsCatYearsDogYears = function(humanYears) {
  let catYears = 0
  let dogYears = 0
  
  if (humanYears == 1){
    catYears = 15
    dogYears = 15
  } else if (humanYears == 2){
    catYears = 15 + 9
    dogYears = 15 + 9
  } else if (humanYears == 3){
    catYears = 15 + 9 + 4
    dogYears = 15 + 9 + 5
  } else {
    catYears = 28 + ((humanYears - 3) * 4)
    dogYears = 29 + ((humanYears - 3) * 5)
    
  }
  
  return [humanYears,catYears,dogYears];
}
```
