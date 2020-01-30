# Data Types and Variables

Variables are containers for holding different types of data. There are only a limited amount of built-in data types the occur in Python programming.

## Variables

Variables hold data! Sometimes you'll want to get data from the user, or manipulate a number multiple times over. In Python, you don't actually have to specify the type for a variable, and you can reuse a variable with something called shadowing.

```python
# assign the letter 'a' to myVar
myVar = 'a'
# overwrite the value of myVar to '5'
myVar = 5
# print the current value of myVar (prints '5')
print(myVar)
```

## Integers

Integers are also known as whole numbers (1, 2, 3, -22, -43). You can specify types for python variables with the following syntax:

```python
myInt: int = 5
```

Because python normally allows variable reuse, this has limited applications. One of those applications could be when you want a variable to *only* hold a certain type of data, and to never hold a different type.

As an example, maybe you have a variable to store the number of times something has occurred. You would only want this variable to be a whole number, since no other data type makes sense.

## Real Numbers/Decimal Numbers (floats)

Floats are also known as Real or Decimal numbers. They have a decimal place, and can have numbers after the decimal. If you want to specify a variable of this type, you would do so like this:

```python
myFloat: float = 3.5
```

## Strings

Strings are sequences of characters, and characters are most typically letters/other symbols. A string can contain 0 or more characters in it. You can specify type as follows:

```python
myString: str = "Hello!"
```

## Boolean Values

Also known as logical values, booleans are either `True` or `False`. They help more in the section on Control Flow. Type for a variable can be specified as follows:

```python
myBool: bool = True
```

[Next](https://github.com/ocoffey/Syntax-Sheets/blob/master/Python/3_User_Interaction.md "User Interaction"), we go over more methods of user interaction.
