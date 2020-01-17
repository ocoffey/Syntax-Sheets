# Control Flow

How you improve code quality and reusability.

## Conditional Statements

Your basic control flow schemes.

### if statement

The first control flow statement. If the condition inside the parenthesis evalutes to true, then the following statement is run. If the condition is false, the statement doesn't run.

```cpp
// Format
if (<condition_goes_here>) {
    // <statement(s)_go_here>
}
```

```cpp
// Example
bool thisIsTrue = true;
if (thisIsTrue) {
    std::cout << "This is true" << std::endl;
}
```

### else statement

Gives an alternative clause for the if statement. When the if statement evaluates to false, the else statement runs.

```cpp
bool falseExample = false;
if (falseExample) {
    // this will not run
}
else {
    // this will run
    std::cout << "This is false" << std::endl;
}
```

### else if statement

Allows for more options within if...else clauses. Sometimes, you want to check for one of many options, with your else statement being a failsafe.

```cpp
int myNum = 2;
if (myNum == 1) {
    // doesn't run
}
else if (myNum == 2) {
    //runs, since myNum is equal to '2'
    std::cout << myNum << std::endl;
}
else {
    // doesn't run
}
```

## Loops

Why write something 100 times if you could write it once and throw it in a loop?
> The 'break' keyword will exit a loop at any time. It is most useful when nested in a conditional statement, so that when the condition is true, the loop will end.

### While Loop

Your most basic loop; it will run until its condition is false.

Ex.1 - Infinite Loop

```cpp
while (true) {
    std::cout << "I will run forever!!!" << std::endl;
}
// since there is no 'break' here, and the condition is always true, this code will never stop running.
```

Ex.2 - Broken Loop

```cpp
while (true) {
    std::cout << "I want to run forever :'(" << std::endl;
    break;
}
// this loop will break just after its print statement
```

Ex.3 - Natural Loop

```cpp
// Normally, loops will have this structure; of having some changing variable, that will
// eventually break the loop
int i = 0;
while (i < 5) {
    i++; // increments i on each iteration, and when i == 5, the loop breaks
}
```

### For Loop

Probably the most common loop you'll use. A for loop takes 3 parameters; a variable that will be changed, a conditional statement to evaluate (which should use the previous variable), and a function to change the variable. These statements are separated by ';'

```cpp
for (int i = 0; i < 10; i++) {
    std::cout << i << ", "; // prints the values of i from 1 to 9, separated by commas and spaces
}
std::endl; // makes a new line
```

### Do While Loop

Probably the least common loop used; its use case is for when you want a statement to run at least once, and then maybe some more. The statement before 'while' will always run before the condition is checked.

```cpp
bool oneRun = true;
do {
    std::cout << "I will only run once, and not loop" << std::endl;
    oneRun = false;
} while(oneRun);
```

## Switch Statements

Related to conditional statements, but divergent. A switch statement compares your input against its possible cases, and runs the case that matches the input (if found). `break` is useful in parts of control.

## default case

<to fill in later>

[Next](https://github.com/ocoffey/Syntax-Sheets/blob/master/C++/6_Complex_Data_Types.md "Complex Data Types"), we cover complex data types.
