# Basic Concepts

- bits/bytes
- variables
- types
- if else
- loops
- functions/methods
- arrays

## Bits / bytes

- a bit is either a 1 or 0;
- 1 byte is 8 zeroes or ones;
- 8 bits are 1 byte;
- Respresents the amount of space on a computer.

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
let hey = "";
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
    ...
else
    ...
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
