# Data Types and Variables

There are different types of data that we need to interact with while programming! Not everything is going to be a number.

## Variables

Variables are containers for values that we wish to manipulate. Think over to math classes, where you have to solve for x or y. In this scenario, x and y are containers for data! <br>
* When a variable is declared, we are telling our computer "make room large enough for this type of data, and keep that spot open!". This space is made in your computers RAM (Random Access Memory).
* When a variable is initialized, we are actively assigning a value to that variable.
> Most of the time in other languages, we would declare and initialize within the same line. The C language likes to have all the variables you will use at least declared at the top of your function, and then initializing/using them afterwards.

## Integers (Non-Fractional, Non-Decimal Numbers)

Integers are numbers without any decimal places. These are the first numbers you learned about when you learned what numbers are (they are "whole numbers"). Creating an integer variable uses the `int` keyword.
```c
#include <stdio.h>

int main(void) {
    int my_integer; // this line makes space in the RAM equivalent to what an int can take up
    my_integer = 5; // this line assigns a value to that space in RAM
    return 0;
}
```
In C, ints take up 4 bytes of memory.
> You might have noticed that an int is the data type our main function is returning! That's where the 'int' comes from on the function line, and is why our return value of 0 corresponds to the type.

## Real Numbers (Decimal Numbers)

Real numbers include integers, but also include decimal numbers! If you assign an integer to a real number's variable, the number will gain a decimal place (5 -> 5.0). Real numbers typically use the `float` keyword.
```c
#include <stdio.h>

int main(void) {
    float my_float; // declares a floating point variable
    my_float = 5.357; // assigns a value to our variabe
    return 0;
}
```
In C, floats take up 4 bytes of memory.

## Logical Values (Truths and Falsehoods)



## Characters (Letters and Symbols)


