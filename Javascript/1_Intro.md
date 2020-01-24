# Introduction to Javascript Language Syntax

An introduction to the basics of Javascript

---

## Output and Input

Printing data to the user, and receiving data from the user.

### User Output

User output in javascript is printed with the `console.log()` method:

```javascript
console.log(97);
console.log("ok computer");
console.log(2 + 2.5);
```

### User Input

Uses the `prompt()` method:
> The data is stored in a variable, which is covered later on.

```javascript
var userName = prompt("What is your name?");
```

## Comments

Similar in syntax to C/C++

### Single-Line Comments

Uses `//`

```javascript
// This will print 'hello' to the user output
console.log("hello")
```

### Multi-Line Comments

Uses `/*` to begin, and `*/` to end.

```javascript
/*
    This section will take user input, store it in a variable,
    and print the value afterwards
*/
var userName = prompt("Please enter your name");
console.log("Your name is ${userName}.");
```

[Next](https://github.com/ocoffey/Syntax-Sheets/blob/master/Javascript/2_Variables.md "Variables"), we cover the syntax for variables.
