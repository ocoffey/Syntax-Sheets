# Functions

So far the examples we've seen have all been in the `main` function. In addition to `main`, we can make our own functions (sometimes referred to as "helper functions"), and also make some of these functions recursive!

---

## User Defined Functions

In C, user made functions need to be defined before they are ever called upon. Because of that, we define our functions above `main`:
```c
#include <stdio.h>

void print_hello() {
    printf("Hello!");
}

int main(void) {
    print_hello();
    return 0;
}
```
As with breaking down `main` previously, we can break down how these user functions are created.

### Format

```c
<return type> <functionname>(<parameter(s), including type(s)>) {
    // stuff and things
    return <element that corresponds to our return type>;
}
```

### Examples

```c
#include <stdio.h>

int add_these(int x, int y) {
    return x + y;
}

int main(void) {
    int i = 2;
    int j = 3;
    printf("%d", add_these(i,j));
    return 0;
}
```
In this example, we declare two variables and initialize them with different values. We then pass those values to our helper function, which adds them together, returns their sum, and uses that sum in the place of `%d`.
```c
#include <stdio.h>

int is_this_a_letter(char c) {
    if (c >= 'A' && c <= 'Z') {
        return 1;
    }
    else if (c >= 'a' && c <= 'z') {
        return 1;
    }
    else {
        return 0;
    }
}

int main(void) {
    char let = 'b';
    int is_letter = is_this_a_letter(let);
    if (is_letter) {
        printf("%c is a letter", let);
    }
    else {
        printf("%c is not a letter", let);
    }
    return 0;
}
```
In this example, we initialize our character variable with the letter 'b'. Then, that letter is passed to our helper function, which checks if 'b' is a capital letter, then a lowercase letter. Since it is a lower case letter, that function returns 1 (or true), which tells our main function to print that 'b' is in fact a letter
> One thing to keep in mind with helper functions is that they consume more memory to invoke. When we call is_this_a_letter(), we're adding another character variable (c) to the stack, which takes up another byte for the duration of the function. This isn't a huge issue now, but will be something to keep in mind for recursion.

## Recursion

Recursion is a tricky concept to understand for budding computer scientists. If you've ever seen the movie Inception, it kind of works like that!<br> Recursion takes a large problem, and breaks it down into smaller, solveable problems!
>Once you get used to using it, recursion is easy for the scientist, but intensive for the computer.

>The kind of examples shown so far are something called Iterative solutions. Iterative coding can be a bit harder for the scientist, but is typically easier for the computer to handle.

### Format

Typically, recursive functions have something called a `base case`; this is a condition that stops the recursion from happening.
```c
<return type> <function name> (<parameter(s)>) {
    if (<base case condition>) {
        // do something
        return something;
    }
    else {
        <function name>(parameter with some variation);
        return something;
    }
}
```

### Examples

Recursion can be difficult to wrap your brain around with just the format alone; examples immensely help comprehension for this.

#### Example 1

```c
#include <stdio.h>

void print_from_zero(int my_number) {
    if (my_number < 0) {
        return;
    }
    else {
        print_from_zero(my_number - 1);
        printf("%d ", my_number);
        return;
    }
}

int main(void) {
    print_from_zero(2);
    print_from_zero(10);
    printf_from_zero(25);
    return 0;
}
```
Recursive coding involves functions that call themselves! In this example, we want to print numbers, starting at 0, that count up to our original integer. Let's look more closely at our call `print_from_zero(2)`:

1. First, we call the function with a value of `2`. Our base case is checked, and since 2 isn't less than 0, our function goes to the `else` statement.
2. At this point, we call our function again, but pass it the value of our variable minus 1 (so a value of `1`), and we start that cycle again.
    >Note: At this stage, our previous function frame is open with a value of 2, and is stalled, waiting for our new function frame to end.
3. In this frame where `my_number` is `1`, we compare against the base case again, and since 1 isn't less than 0, we go to the else statement again. Here, we call our function again, with a value of `my_number` - 1, or `0`.
4. The process continues again; we don't meet our base case, and call the function passing a value of `-1`.
    >At this point, our previous frames our still open, with values of `2`, `1`, and `0` respectively. We just opened a new frame with a value of `-1`
5. Here, we check against our base case, and finally meet the base case! Because of this, we return up a frame (where `my_number` is `0`), and continue doing the instructions that we can.<br> In this example, that means printing the value of `my_number`, followed by a space.
6. After printing, we return up another frame, where `mynumber` is `1`, print it followed by a space, and return up to our last recursive frame, with `my_number` equal to `2`.
7. Finally, we print the value of our number (`2`), and return out into the main function!
> After this, we follow the same steps for printing up to 10 and 25 respectively.

In this example, we could have more easily accomplished this goal iteratively, as so:
```c
void print_from_zero(int my_number) {
    for (int i = 0; i <= my_number; i++) {
        printf("%d", i);
    }
}
```
So in this case, our iterative solution was much easier to implement, and would be easier for our computer to run. This isn't the case for all problems, but it is hard to come up with examples that prove recursion's usefulness without treading toes on examples your professors would use :)

#### Example 2

Say you wanted to print a right-leaning pyramid with hashtags (`#`). Although this can be done iteratively, a recursive example shows how it may be easier to understand parts of the solution more easily.
>This example shows how a function can be split into many helper recursive functions
```c
#include <stdio.h>

void print_spaces(int numspaces) {
    if (numspaces == 0) {
        return;
    }
    else {
        printf(" ");
        print_spaces(numspaces - 1);
        return;
    }
}

void print_hashes(int numhashes) {
    if (numhashes == 0) {
        return;
    }
    else {
        printf("#");
        print_hashes(numhashes - 1);
        return;
    }
}

void print_pyramid(int spaces, int hashes) {
    if (spaces < 0) {
        return;
    }
    else {
        print_spaces(spaces);
        print_hashes(hashes);
        printf("\n");
        print_pyramid(spaces - 1, hashes + 1);
        return;
    }
}

void print_mypyramid(int height) {
    print_pyramid(height - 1, 1);
    return;
}

int main(void) {
    print_mypyramid(5); 
    return 0;
}
```
1. First, we call a helper function, `print_mypyramid()`. This function takes how tall we need to print the pyramid, and calls `print_pyramid()` with appropriate parameters (the first line for a pyramid will have height - 1 spaces, and 1 hashtag).
    > If we were using C++, we could make use of something called overloading a function, which would allow us to let `print_pyramid()` and `print_mypyramid()` have the same name. The reason we include `print_mypyramid()` at all is to help understanding; that we just enter a height of 5, and then the helper splits this into algorithm-relevant info.
2. Next, within `print_pyramid()`, we're printing the spaces and hashes for the first line (using recursive helper functions that print each respectively), a newline, then changing the values of spaces and hashes for the next line and calling that function!
3. In this function, our base case triggers when we hit a negative number of spaces, which would occur after our last line prints.