# Introduction to C++ Language Syntax

An introduction to the basics of C++

---

## Explaining the `main()` Function

This is a small example of a C++ program that prints 'ok computer' to the console. Following the code snippet is a breakdown of each part of the code.

```cpp
#include <iostream>

int main(void) {
    // this next line will print the words 'ok computer' to the console
    std::cout << "ok computer" << std::endl;
    return 0;
}
```

### `#include <iostream>`

Many times in programming, a previous programmer has written code that we can make use of, instead of us trying to write an entire program from ground 0! We use `#include` to reference libraries of code that others have written. `#include` can also be used to reference other pieces of code that you write!

In this case, `<iostream>` is a library that defines some basic functions the we use for printing to the console.

### `int main(void)`

In C++, `main()` is the name of a special function that we use to actually run our code. If our code isn't in `main()`, then it won't occur. There are ways in which you can clump pieces of code together to make `main()` look more succinct, which appears later in this guide.

### { } [Curly Brackets]

In C++, code blocks need to be surrounded by curly brackets. Looking at the example above, you can see that a curly bracket opens just after `int main(void)`, and that a second, closing bracket occurs as our last line of code. These brackets work as a sort of container for this section of code, so when the code is compiled, the compiler can go "okay, we'll use everything that's between those brackets".

### Comments: Single Line `//` and Multi-Line `/* */`

Comments have many purposes. The main purpose is to explain what parts of the code are doing. If you're only trying to explain a small snippet of a line, you'd typically use a single line comment:

```cpp
// This next line of code does <something>
```

Multi-Line comments are typically used for larger descriptions, like what a whole section of code is going to be doing:

```cpp
/*
    This simple program will print 'ok computer' to the standard output.
    The program is meant to showcase a simple interaction of elements in C++.
*/
```

> Tip: commenting can also be used to temporarily undo problem sections of your code. If you're adding a new section that's giving you issues, you can comment out small sections that you think might be causing the issue, which allows you to pinpoint the problem area.

### `std::cout << "ok computer" << std::endl;`

This section prints "ok computer" to the standard output. Originally in computers, programming was done entirely with a keyboard, and everything was text-based. The standard output is a remnant of this; a simple, text-based output system. The `cout` section means "print this to the *standard character output*", while the `endl` section means "end line"; akin to pressing 'enter' on your keyboard.

### `return 0;`

In C++, all functions have to return some type of value. A return of 0 in C++ lets the program know that `main` completed without any issues. Looking back at our definition for `main`, we can actually see that the return type is declared at the beginning of `int main(void)`, namely an integer type. Integers will be covered later, but at its base, it means that main is expecting a number to be returned.

## Statements

Each line of our code within our function is a statement. All statements in C++ end with a semicolon [ ; ]. If you do not have a semicolon at the end of your statement(s), your program can behave erratically, or simply not compile.

[Next](https://github.com/ocoffey/Syntax-Sheets/blob/master/C++/2_User_Interaction.md "User Interaction"), methods of user interaction are covered.
