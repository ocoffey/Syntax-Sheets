# Basic Functions

Some of the functions to use that are received from the ```cpp<iostream>``` header.

## Printing Output to Console

If you used C before now, rejoice! Printing output is far easier in C++. You must specify that you are using the std (standard) namespace in order for this to work.
```cpp
std::cout << "This is printing" << std::endl
// You can also replace specific words inbetween '<<' with variables!
std::String word = " also ";
std::cout << "This " << "is" << word << "printing" << std::endl;
```

## Receiving Input from Console

Uses the cin keyword, and stores the input into a variable.
```cpp
int usernum;
std::cout << "Please enter a number" << std::endl;
std::in >> usernum;
std::cout << "You entered: " << usernum << std::endl;
```
If a user enters input that isn't of the type you're expecting, you will receive an error.



# Basic Data Types and Operators

These are the basic types of variables, operators for those variables, and their syntax

## Data Types

Your basic data types

### int

Your basic integer numeric data type. Integers are non-decimal numbers. Default use of int creates a signed integer (the integer can have negative values). You can also specify to create a variable as an unsigned integer. Integers use 4 bytes of data in C++.
```cpp
int my_int = 5;
my_int = -3;
std::cout << my_int << std::endl;
// prints -3
```

### float

Your basic real numeric data type. Real numbers include decimal numbers. Floats do not have the option to be unsigned. Floats use 4 bytes of data in C++.
```cpp
float my_float = 17.5;
my_float = 3;
std::cout << my_float << std::endl;
// prints 3.0
```

### bool

Your logical data type. Can only hold the values ```true``` or ```false```. If you assign a non-zero numeric value to a bool, the bool variable will hold the value ```true```. Bools use 1 byte of data.
```cpp
bool thisIsTrue = false;
thisIsTrue = true;
if (thisIsTrue) {
    std::cout << "The value was true" << std::endl;
}
// prints the sentence since the boolean variable was true. if statements will be covered more later.
```

### char

Your symbolic data type. Characters are actually numeric values, that are looked up on the ascii table within C++. You can apply mathematical operations to them to change their values. Chars use 1 byte of data.
```cpp
char myInitial;
std::cout << "Please enter the initial of your last name" << std::endl;
std::cin >> myInitial;
std::cout << "The initial of your last name is: " << myInitial << std::endl;
```

## Logical and Mathematical Operators

Used to manipulate values and check for equalities.

### Mathematical Operators

#### +

Basic addition operator

#### -

Basic subtraction operator

#### *

Basic multiplication operator

#### /

The integer division operator. This operator effectively uses long division, and returns your answer without the remainder.
```cpp
a = 5 / 2;
// a has a value of '2'
```

#### %

The remainder operator (known as modulo/modulus). This operator will output *only* the remainder of the division operation. This operator is very useful for checking if a number is odd or even (by doing num % 2), and other functions of that nature.
```cpp
a = 5 % 2;
// a has a value of '1', or the remainder of 5 / 2
```

#### ==

The mathematical equality operator. A single '=' would assign a value to a variable, so '==' is used to compare equality instead.
```cpp
bool areTheseEqual;
areTheseEqual = (17 == 8); // assigns true or false, dependent on the comparison (so false)
areTheseEqual = (12 == (4 + 8)); // assigns true
```

### Logical Operators

#### &&

The logical 'and' operator. This operator checks to see that both sides of the equation logically evaluate to true.
```cpp
bool truthTest;
truthTest = (true && true);
// truthTest has a value of true, since the expression was true for both of its sides
truthTest = (1 && 5);
// this would also make truthTest true, since non-zero values are considered true
// (any non-zero value is considered true, and zero is false)
```

##### && Truth Table

|   A   |   B   | Result |
|  ---  |  ---  |  ---   |
| true  | true  | true   |
| true  | false | false  |
| false | true  | false  |
| false | false | false  |

#### ||

The logical 'or' operator. This operator checks to see if either side of the equation logically evaluates to true.
```cpp
bool isThisTrue;
isThisTrue = (true || false);
// isThisTrue has a value of true, since one of the sides was true
isThisTrue = (10 || 0);
// also makes isThisTrue to true, since one of the sides is non-zero
```

##### || Truth Table

|   A   |   B   | Result |
|  ---  |  ---  |  ---   |
| true  | true  | true   |
| true  | false | true   |
| false | true  | true   |
| false | false | false  |



# Containers (Advanced Data Types)

These data types are serializations of other data types

## Arrays

## Strings



# Control Flow

## Conditional Statements

### if statement

### else statement

### else if statement

## Switch Statements

## Loops

### While Loop

### For Loop

### Do While Loop



# Functions

## Parameters

## Return Values

## Scope

## Iterative Functions

## Recursive Functions



# Pointers and Dynamic Programming



# Classes