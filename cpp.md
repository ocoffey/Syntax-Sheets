# Basic Functions
Some of the functions to use that are received from the ```<iostream>``` header.
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

# Basic Data Types and Operators
These are the basic types of variables, operators for those variables, and their syntax
## Data Types
Your basic data types
### int
Your basic integer numeric data type. Integers are non-decimal numbers. Default use of int creates a signed integer (the integer can have negative values). You can also specify to create a variable as an unsigned integer.
```cpp
int my_int = 5;
my_int = -3;
std::cout << my_int << std::endl;
// prints -3
```
### float
Your basic real numeric data type. Real numbers include decimal numbers. Floats do not have the option to be unsigned.
```cpp
float my_float = 17.5;
my_float = 3;
std::cout << my_float << std::endl;
// prints 3.0
```
### bool

### char

## Operators

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



# Pointers and Dynamic Programming



# Classes