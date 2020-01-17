# Basic Data Types

These are the basic types of variables in C++, and also the operator that makes it all happen.

## Assignment Operator

The syntax for assignment is fairly equivalent among languages; the '=' sign is used to assign values to variables. It takes the value of whatever is on the right hand side, and assigns that value to whatever is on the left hand side.

```cpp
int a;
a = 5; // writes the value of '5' into the memory location of a. More on those later;
       // the takeaway is that 'a' now holds a value of '5'
```

## Data Types

Your basic data types

### int

Your basic integer numeric data type. Integers are non-decimal numbers. Default use of `int` creates a signed integer (the integer can have negative values). You can also specify to create a variable as an unsigned integer. Integers use 4 bytes of data in C++.

```cpp
// declaring the variable my_int, and initializing it with a value of '5'
int my_int = 5;
// overwriting the value within my_int to '3'
my_int = -3;
// printing the contents of my_int, to see what it now holds
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

Your logical data type. Can only hold the values `true` or `false`. If you assign a non-zero numeric value to a bool, the bool variable will hold the value `true` (anything other than 0 is 'true'). Bools use 1 byte of data.

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

[Next](https://github.com/ocoffey/Syntax-Sheets/blob/master/C++/4_Operators.md "Operators"), more operators are covered.
