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
Sometimes though, we won't always know exactly what we're going to print at our time of writing, which is why we also have something called format specifiers.

### Format Specifiers

Format specifiers occur inline with the text we print, and tell `printf` that some part of the text is going to be replaced. This is useful for times when we compute something based on user input, and want to tell the user what we found.
```c
#include <stdio.h>

int main(void) {
    printf("This will print the number three: %d", 3);
    // In this example, the '%d' is replaced with our number 3!
    return 0;
}
```
> There is a list of format specifiers [here](http://www.cplusplus.com/reference/cstdio/printf/ "List of Format Specifiers").

## Receiving Input from the Console

Conversely to printing output, we also are able to receive input in C; input is received with the `scanf()` function.

### `scanf()`

`scanf()` will allow the user enter an input, which we can then store to use for our calculations!