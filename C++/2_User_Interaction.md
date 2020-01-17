# User Interaction

There are two main types of user interaction, with those being printing output to the user, or receiving input from the user.

## Printing Output to Console

If you used C before now, rejoice! Printing output is far easier in C++. You must specify that you are using the std (standard) namespace in order for this to work.

```cpp
std::cout << "This is printing" << std::endl;
// You can also replace specific words inbetween '<<' with variables!
std::String myWord = " also ";
std::cout << "This " << "is" << myWord << "printing" << std::endl;
```

To expand upon the previous page, `cout` will print everything that occurs after the double bracket (`<<`). This can be words, or potentially other built in methods, like `endl`.

> The line that has 'String' will be explained in depth later. It's a variable, or storage container. In this case, a 'String' stores letters, and can hold a word.

## Receiving Input from Console

Uses the `cin` keyword, and stores the input into a variable. `cin` stands for "character input".

```cpp
// Here, userNum is a container that will hold the users number.
int userNum;
// It can be useful to prompt the user for input, with specifications
// of what you're looking for
std::cout << "Please enter a number" << std::endl;
// Whatever the user types in is stored into our variable
std::cin >> userNum;
// Since the variable is holding what the user put it, this statement
// will print that word out to them!
std::cout << "You entered: " << userNum << std::endl;
```

If a user enters input that isn't of the type you're expecting, you will receive an error. Checking for correct type is something that will be learned later.

[Next](https://github.com/ocoffey/Syntax-Sheets/blob/master/C++/3_Data_Types.md "Data Types"), data types are explained more in depth.
