# Basic Operators

Operators that don't quite fit other categories.

## Assignment Operator

The `=` is the assignment operator. This operator works from right to left, taking the value on the right of the operator, and assigning that value to the variable on the left.
```c
int main(void){
    int myval = 1; // This line sets the value of myval to 1 (instantiation)
    // This next part takes the previous value of myval, adds 5,
    // and assigns the total value of 6 to myval
    myval = myval /*<- current value is 1*/ + 5;
    // The value after reassignment is 6
    printf("%d\n", myval);
    return 0;
}
```

# Basic Mathematical Operators

For basic mathematical operations

## +

Basic addition operator

## -

Basic subtraction operator

## *

Basic multiplication operator

## /

The integer division operator. This operator effectively uses long division, and returns your answer without the remainder.
```c
int main(void) {
    int a;
    a = 5 / 2;
    // a has a value of '2', since 5/2 is '2' with remainder '1'
    return 0;
}
```

## %

The remainder operator (known as modulo/modulus). This operator will output *only* the remainder of the division operation. This operator is very useful for checking if a number is odd or even (by doing num % 2), and other functions of that nature.
```c
int main(void) {
    int a;
    a = 5 % 2;
    // a has a value of '1', or the remainder of 5 / 2
    return 0;
}
```

# Advanced Mathematical Operators

For advanced/time-saving mathematical operations

## Increments and Decrements

For when you need to quickly add or subtract 1 from a value

### ++

Increments the variable by one. Frequently used in loops to increment a counter variable. Can be done either before or after the value; where you use it will affect when the increment occurs

#### `var++`

```c
int main(void) {
    int i = 1;
    // This print statement will print '1'
    printf("%d\n", i++);
    // This print statement will print '2'
    printf("%d\n", i);
    // This occurs because for the first statement, <var>++ will
    // print the current value of i, and then increment that value.
    // This makes it so that when we print the value the second time,
    // it will have reflected that change
    return 0;
}
```

#### `++var`

```c
int main(void) {
    int i = 1;
    // This print statement will print '2'
    printf("%d\n", ++i);
    // This print statement will also print '2'
    printf("%d\n", i);
    // As can be expected, this occurs because our increment happens before
    // the value is actually used by the `printf()` function
    // The distinction is useful, and might cause problems in your code
    // if you don't take that difference into account
    return 0;
}
```

### --

Follows the same conventions as ++, in regards to appearing before or after the variable, and the differences each has.

## Mathematical Shortcut Operators

These operators can help for operational shortcuts, where applicable

### +=

This operator is a shortcut of saying `x = x + value`.
```c
int main(void) {
    int i = 2;
    i += 3; // changes the value of i to 5
    return 0;
}
```

### -=

Same as +=, but for subtraction.

### *=

Same as +=, but for multiplication.

### /=

Same as +=, but for integer division.

### %=

Same as +=, but for modulus.

# Logical Statement Evaluators

Logical evaluations use both mathematical and logical operators.

## Mathematical Comparison Operators

For checking mathematical comparisons. After the comparison, these statements will evaluate to either `true` or `false`.

### ==

The equality operator. This operator checks to see that both sides of the equation are equal. If they are, then this statement evaluates to `true`.
```c
int main(void) {
    int mynum = 4;
    // if statements check to see if statement inside parenthesis is true;
    // if it is, then the code within the statement will run
    if (5 == 5) { // 5 is equal to itself, so the condition evaluates to true
        printf("They are equal");
    }
    if (5 == mynum) { // 5 is not equal to 4, so this evaluates to false
        printf("This will not print");
    }
    return 0;
}
```
> We haven't fully covered control flow, so I will just be using `if` statements for these explanations. If you want to cover control flow first, feel free to skip ahead, and then come back

### !=

The inequality operator. This operator will evaluate to `true` if the values on either side *do not* equal each other.
```c
int main(void) {
    int mynum = 17;
    if (3 != 3) { // Doesn't print, since 3 is not unequal to itself
        printf("This will not print");
    }
    if (3 != mynum) { // This prints since 3 is not equal to 17
        printf("This will print");
    }
    return 0;
}
```

### >, >=

These operators check to see if the left side is greater than, or greater than/equal to the right side (respectively). If that is the case, these statements will evaluate to `true`.
```c
int main(void){
    int myval = 5;
    if (myval > 4) {
        printf("This will print.");
    }
    if (myval >= 5) {
        printf("This will also print");
    }
    return 0;
}
```

### <, <=

Follows the same logic as the previous operators, except checking for greater values on the right side of the operator.

## Logical Operators

These operators are used for boolean values of `true` and `false`. These operators can also be combined to form complex evaluations.

### !

The logical 'not' operator (logical inverse). It turns true (nonzero) values false (to zero), and false values true. It does this mathematically, by changing any non-zero value to 0, and values of 0 to 1.
```c
int main(void) {
    int thisWillBeTrue = 0; // Currently this value is logically false
    if (!thisWillBeTrue) { // This statement prints, since the 0
        printf("It's true\n"); // is turned into a 1
    }
    return 0;
}
```

### && (Logical And)

The logical 'and' operator. This operator checks to see that both sides of the equation logically evaluate to be true.
```c
int main(void) {
    int myval = 6;
    if (5 && (myval >= 1)) {
        printf("This evaluated as true\n");
    }
    return 0;
}
```
> You can nest statements with parenthesis, which will evaluate first. Here, 6 is greater than or equal to 1, so that statement evaluates to true (1), and then both 5 *and* 1 are nonzero, so the compound statement evaluates to true, allowing the if statement to run.

#### && Truth Table

A handy table for tracking whether the statements should evaluate as true or false.
|   A   | and |   B   | ->  | Result |
|  ---  | --- |  ---  | --- |  ---   |
| true  | and | true  | ->  | true   |
| true  | and | false | ->  | false  |
| false | and | true  | ->  | false  |
| false | and | false | ->  | false  |

### || (Logical Or)

The logical 'or' operator. This operator checks to see that either side of the operator is a non-zero value, and if there is one, evaluates to 'true'.
```c
int main(void) {
    if (1 || 0) {
        printf("One of the values was true, so this printed\n");
    }
    return 0;
}
```

#### || Truth Table

|   A   | or  |   B   | ->  | Result |
|  ---  | --- |  ---  | --- |  ---   |
| true  | or  | true  | ->  | true   |
| true  | or  | false | ->  | true   |
| false | or  | true  | ->  | true   |
| false | or  | false | ->  | false  |

[Next](https://github.com/ocoffey/Syntax-Sheets/blob/master/C/5_Control_Flow.md "Control Flow"), we will more thoroughly explore control flow past the `if` statement.