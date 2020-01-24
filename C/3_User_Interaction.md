# Basic User Interface Functions

How to interact with the user of your program

## Printing to the Console

Many times in coding, we will need to let the user know some result that our code computed. In C, this is done with the `printf()` function.

### `printf()`

The `printf()` function prints whatever you end up putting inside the parenthesis!

```c
#include <stdio.h>

int main(void) {
    printf("These are the words that the user will see.");
    return 0;
}
```

Sometimes though, we won't always know exactly which values we're going to print at our time of writing, which is why we also have something called format specifiers.

### Format Specifiers

Format specifiers occur inline with the text we print, and tell `printf` that some part of the text is going to be replaced. This is useful for times when we compute something based on user input, and want to tell the user what we found.

```c
#include <stdio.h>

int main(void) {
    printf("This will print the number three: %d", 3);
    // In this example, the '%d' is replaced with our number 3!
    int mynum = 5;
    printf("This will print the number five: %d", mynum);
    // And in this example, the %d is replaced with our variable integer!
    return 0;
}
```

> There is a list of format specifiers [here](http://www.cplusplus.com/reference/cstdio/printf/ "List of Format Specifiers").

## Receiving Input from the Console

Conversely to printing output, we also are able to receive input in C; input is received with the `scanf()` function.

### `scanf()`

`scanf()` will allow the user enter an input, which we can then store to use for our calculations!

```c
int main(void) {
    int usrnum; // This example makes space for an integer
    printf("Please enter a number: "); // Then prompts the user for input
    scanf("%d", &usrnum);   // And finally takes the user input, and stores
                            // the number into our variable
    return 0;
}
```

`scanf()` uses the same list of format specifiers as `printf()`

> You might have noticed the `&` symbol used in front of our variable in `scanf`. This is something called a reference, and will be explored more in depth later. At this stage, just know that you need to place it in front of your variable name in order for `scanf` to work.

[Next](https://github.com/ocoffey/Syntax-Sheets/blob/master/C/4_Operators.md "Operators"), we look at different types of operators!