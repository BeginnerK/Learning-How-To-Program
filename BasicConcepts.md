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

#### method Syntax

```ruby
def sqrt(a) do
    return a**0.5
end

def squared(a) do
    return a**2
end

# lambda
(a) -> a**2
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

console.log(three() % four()); // 0.75
```

#### Modulo (Remainder) (%)

```javascript
function three() {
  return 3;
}

function four() {
  return 4;
}

console.log(three() + four()); // 3
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
print(three <= 3 && iAmBeautiful && 1 >= 0) # true
print(three <= 3 && iAmBeautiful && 1 <= 0) # false
print(three <= 4 && iAmBeautiful && 1 >= 0) # true
print(three <= 0 && iAmBeautiful && 1 >= 0) # false
```

#### Logical OR (||)

```ruby
three = 3
iAmBeautiful = true

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
    calculatePowersOfTwo.push(poweroftwo);
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
  
  for ( let counter = 0; counter < arr.length; counter++){
    if (arr[counter] > 0){
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
  
  let noduplicates = new Set(a) ;
  let array = Array.from(noduplicates);
  
  return array;
}
```
