# Control Flow

Sometimes you want a section of code to execute only if certain conditions are met, and other times you want to re-run a section multiple times! This is where control flow comes into play.
> From here on out, I will not be including the int main(void) {} section for our code. Consider it implicitely there and include it for if you run these examples on your own.

# Conditional Statements

The basic control flow gates of `if`, `else if`, and `else`.

## `if` statement

The first control flow statement. If the condition inside the parenthesis evalutes to true, then the following statement is run. If the condition is false, the statement doesn't run.

### Format

```c
if (<condition_goes_here>) {
    <statement(s)_go_here> // These execute if the condition was true
}
```

### Example

```c
int thisIsTrue = 1;
if (thisIsTrue) { // Non-zeros are logically true in C, so this runs
    printf("The condition was true.\n");
}
```

## `else` statement

Gives an alternative clause for the if statement. When the if statement evaluates to false, the else statement will run instead.
```c
int falseExample = 0;
if (falseExample) {
    // this will not run
}
else {
    // this will run
    printf("The condition was false.\n");
}
```

## `else if` statement

Allows for more options within if...else clauses. Sometimes, you want to check for one of many options, with your else statement being a failsafe.
```c
int myNum = 2;
if (myNum == 1) {
    // doesn't run
}
else if (myNum == 2) {
    //runs, since myNum is equal to '2'
    printf("The condition for this else if statement was true\n");
}
else {
    // doesn't run
}
```

# Loops

Repeatable control flow gates of `while`, `for`, and `do while` loops.
> The 'break' keyword will exit a loop at any time. It is most useful when nested in a conditional statement, so that when the condition is true, the loop will end.

## `while` loops

Your most basic loop; it will run until its condition is false. <br>
> Note: By putting a '1' in our conditional space, we are telling the loop that our condition is always true.
Ex.1 - Infinite Loop
```c
while (1) {
    printf("I will run forever!!!\n");
}
// since there is no 'break' here, and the condition is always true,
// this code will never stop running.
```
Ex.2 - Broken Loop
```c
while (1) {
    printf("I want to run forever :(\n");
    break;
}
// this loop will break just after its print statement
```
Ex.3 - Natural Loop
```c
// Normally, loops will have this sort of structure; 
// of having some changing variable, that will eventually break the loop
int i = 0;
while (i < 5) {
    i++; // increments i on each iteration, and when i == 5, the loop breaks
}
```

## `for` loops

Probably the most common loop you'll use. A `for` loop takes 3 parameters:
1. A variable that will be changed
2. A conditional statement to evaluate (which typically will use the changing variable)
3. A function to change the variable (incrementing, decrementing, or something else)

These statements are separated by a semicolon.

### Format

```c
for (<variable initialization>; <conditional statement>; <variable increment> {
    // do stuff
}
```

### Example

```c
int i; // declared but uninitialized
for (i = 0; i < 10; i++) {
    printf("%d, ", i);  // prints the values of i from 0 to 9,
                        // separated by commas and spaces
}
printf("\n"); // makes a newline after the loop completes
```

## `do while` loops

Probably the least commonly used loop; its use case is for when you want a statement to run at least once, and then maybe some more after that. The statement before 'while' will always run before the condition is checked for its first time.
```c
int oneRun = 1;
do {
    printf("I will only run once, and not loop\n");
    oneRun = 0;
} while(oneRun); // evaluates to false, and doesn't run again
```

[Next](https://github.com/ocoffey/Syntax-Sheets/blob/master/C/6_Complex_Data-Types.md "Complex Data Types"), we explore some examples of complex data types.