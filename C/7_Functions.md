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
<return type> <functionname>(<parameters, including types>) {
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