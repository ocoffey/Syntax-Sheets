# Introduction to C Language Syntax

An introduction to the basics of C

---

## Explaining the Main Function

This is an example of a small program in C (which in this case, does nothing). I'll break down what each part is after the example.
```c
#include <stdio.h>

int main(void) {
    // do things
    return 0;
}
```

### `#include <stdio.h>`

The first line, `#include <stdio.h>`, is including an external library for our program; external libraries have predefined functions, which we can access!
> Libraries save us time in programming by us not having to rewrite every trival operation; imagine having to personally write the methods for getting user input every time you wanted it (it would be awful)

### `int main(void)`

The first part, `int`, is specifying the type of the return value (we'll find out more about types and return values in a bit). <br>
The second part, `main()`, is a special named function; it tells our program where to start running the code from. <br>
Our third part, `void`, is something called a parameter; in this scenario, we're saying that our function doesn't use any parameters (you can numerically think of void as 0).

### Brackets { }

Brackets tell our main function where the code we are going to run is going to be contained. <br>
An opening bracket occurs after a function definition, and a closing bracket occurs at the end of the function.
> Fun Fact: Brackets define something called a "namespace", but you won't really need to know about that until CSC 301

### Comments: Single Line `//` and Multi-Line `/* */`

The line under `int main(void)` is the line `// do things`. Two forward slashes denotes a single line comment; comments are useful for explaining what that section of code is trying to do. This is both useful for coordinating coding with other programmers, and for yourself, in case you revisit old code and forgot what it was doing. You can also do multi-line comments like so:
```c
/*  Multi-Line
    Comments */
```
While your executable program is being made from your .c file, the compiler will remove all of your comments, since they aren't needed for running the program. The comments will still remain in your original .c file.
> Comments also have the useful function of being able to temporarily render lines of code inert; if you are testing code and are having issues with one section, you can comment that section out and work on other sections, allowing you to return later to the problem area

### `return 0;`

In C, every function needs some return value. Return values let other parts of the program know that this part is done with what it needed to do! <br>
The `main()` function is special, in that it specifically needs you to `return 0` when your program is done; this lets your program know that it successfully ran. If you were to return a different number, you would get an error.

### Statements

Technically, us putting `return 0;` is something called a statement; statements end in a `;`. Statements let our program know how many operations to try and do before moving on to the next set of them; typically, you will use a semicolon at the end of each line of your code.

Next, we need to learn the different types of data, and containers for storing them (variables).