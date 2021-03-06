# Complex Data Types

Some data types are made up of smaller data types that are next to each other. The example we'll go over are called arrays.

## Arrays

A series of one type of data, which can be useful for when you need to store or manipulate multiple inputs of the same type. Arrays are zero-indexed (the first element is at index 0). In C, you can reference elements past the size of the array, which will give a whole slew of errors.
> If you've used strings before, strings are an array of characters.


### Format

```c
<data type> <array name> [<length of the array>];
```

### Declaring, then Initializing

This example declares the array (making the space for it in RAM), and then initializes the values within the array
```c
int myarr[10]; // declares an array of size 10, which can only hold integers
int i;
// This loop will set each index to its corresponding numeric value 
for (i = 0; i < 10; i++) {
    myarr[i] = i;   // specific elements in the array are accessed with
                    // brackets just after the name of our array
}
```

### Declaring and Initializing in one step

This example declares and initializes the array in the same step (akin to `int i = 5`). You must use curly brackets to place your initial values.
```c
int myarr[3] = {0, 1, 2};
```
> Note: If you declare an array but don't initialize a value before you reference it, C will allow you to, but you will get 'garbage values'. This is because declaration chooses free space that's available in RAM, but there are still values in those cells from previous operations. Make sure to only reference parts of your array that you have already overwritten.

### Visualization

A visualization of our previous example. Somewhere in RAM, we would have something that looks kind of like this:

**myarr**

|Index|  0  |  1  |  2  |
|  -  |  -  |  -  |  -  |
|Value| `0` | `1` | `2` |

> If you remember from the data types section, integers take up 4 bytes of memory, so our full array takes up 12 bytes!

## Strings

A special type of array made of characters. In C, strings are an array that ends with the null character (`'\x0'`, or `'\0'` from the ASCII table, or the numeric value `0`). This lets us know when our string ends, and so, we need to create character arrays with one extra space (for us to store the null character).

### Getting a string from the user

Here, we will declare a string, and then accept the string that the user inputs.
```c
char myString[11];
printf("Please enter a string that is 10 characters or less");
scanf("%s", myString);
```
> In this example, we make a character array of size 11, and ask for a string that is 10 or less characters. This is because we need space for our null character. The string format specifier for `scanf` will take user input, and automatically append the null character wherever our input ends. If the user enters more than 10 characters, `scanf` will take the first 10 characters only, add the null character, and discard the rest.

### Visualization

Let's say that the user entered "hello" in our previous example; somewhere in our RAM, our string would look kinda like this:

|Index|  0  |  1  |  2  |  3  |  4  |  5  |  6  |  7  |  8  |  9  |
|  -  |  -  |  -  |  -  |  -  |  -  |  -  |  -  |  -  |  -  |  -  |
|Value|`'h'`|`'e'`|`'l'`|`'l'`|`'o'`|`'\x0'`|trash|trash|trash|trash|

> Even though the values at the end of our array are unknown, they still take up space because we told the RAM that we needed the space.

[Next](https://github.com/ocoffey/Syntax-Sheets/blob/master/C/7_Functions.md "Functions"), we explore some examples of user defined (helper) functions, then recursive functions.