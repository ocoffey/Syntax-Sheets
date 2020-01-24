# User Interaction

Printing to the console, and receiving input from the user.

## Printing to the Console

As mentioned earlier, we use the `print()` function to print data to the console. There are, however, a couple of additional tricks that are useful to know.

### Printing variables inline - specifiers

Sometimes, you will want to print data from variables within a print statement. To do this, you can put format specifiers in the areas of your print statement that you want the variables to appear.

```python
myNum = 2
myWord = "hey"
print("My number was: %d and my word was: %s" % (myNum, myWord))
```

This is a quick list of format specifiers for data types:

| Specifier |  Data Type            |
|    ---    |  ---                  |
| `d`, `i`  |  Integer              |
| `e`, `E`  |  Float (exp. format)  |
| `f`, `F`  |  Float (dec. format)  |
| `c`       |  Single character     |
| `s`       |  String               |

>Specifiers are all preceeded by a `%`

### Printing variables inline - concatenation

You can also print variables within your `print()` function by using string concatenation. This makes use of the `+` operator in between the separate strings.

```python
myNum = 2
myWord = "hey"
print("My number was: " + str(myNum) + "and my word was: " + str(myWord))
```

> The `str()` function takes an input, and converts it to a string.

## Receiving User Input

You can receive input from the user with the `input()` function. Depending on the scope of your code, you might want to prompt the user to input something, as the `input()` function won't do this by default. Most times, you will want to assign the user's input to a variable.

```python
userName: str = input("Please enter your name: ")
print("Your name is: " + userName)
```

[Next](https://github.com/ocoffey/Syntax-Sheets/blob/master/Python/4_Operators.md "Operators"), we go over different types of operators that are used in python.
