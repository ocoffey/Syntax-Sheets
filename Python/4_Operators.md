# Operators

Mathmatical, Logical, and otherwise.

## Assignment Operator

The `=` sign. Used to assign values to variables.

```python
# Earlier examples already showed this occurring,
# however, you can also do multiple assignments in one
a = 5
b = a
c = d = e = 10
# prints '5, 5'
print(str(a) + ", " + str(b))
# prints '10, 10, 10'
print(str(c) + ", " + str(d) + ", " + str(e))
```

## Mathmatical Operators

### Basic Operators

Mostly the same as in math courses.

#### `+`

Works as expected.

```python
a = 5
a = a + 3
# prints 8
print(a)
```

#### `-`

Works as expected.

#### `*`

Works as expected.

#### `/`

Regular division that works as expected. If an integer is divided, it might turn into a float.

```python

```

#### `//`

Works a little differently than expected. It uses integer division (think long division), and will give the integer division amount without remainder.

```python
a = 5
a = a // 2
# a is now 2, because although 5/2 is 2.5,
# 5//2 gives the floor of 2.5, being 2
print(a)
```

#### `%`

Modulus/Modulo. Gives __*only*__ the integer remainder from a division operation.

```python
a = 5
# takes a//2's remainder, which is 1
a = a % 2
# prints '1', because 5 is an odd number
print(a)
```

### Compound Operators

#### `+=`

A shortcut for incrementing by an amount. The following example is equivalent.

```python
a = 2
# increasing 'a' by 3
a = a + 3
b = 2
# increasing 'b' by 3
b += 3
# prints '5' twice
print(a)
print(b)
```

#### `-=`

Works similarly to `+=`.

#### `*=`

Works similarly to `+=`.

#### `/=`

Works similarly to `+=`.

### Mathematical Comparison Operators

For use in mathematical comparisons.

#### ==

Equality. Checks to see that the value on the right is equivalent to the value on the left.

```python
a = 5
# this assert is true, since a is 5
assert(a == 5)
```

#### !=

Not equals. Checks to see that the values on the right and left are unequal.

```python
a = 2
assert(a != 7)
```

#### <, <=

Less than/less than or equal to. Works the same as it does in math.

```python
a = 1
assert(a <= 9)
```

#### >, >=

Comparable to the previous example, just in the other direction.

## Logical Operators

For logical comparisons. Python added more plaintext functionality, with all of these operators having a plaintext equivalent keyword. With this, we'll be having a slight introduction to the `if` statement, which is gone over more in the Control Flow section.

### `!` / `not`

Inverts the truth of expressions. It makes False True, and True False.

```python
# if the statement after the 'if' is true,
# then the inner statement code will run.\
if not False:
    print("It's true.")
```

### `&&` / `and`

Logical 'and'. Is true if both sides of the equation are true. For a full breakdown of options, view the Truth Table below.

```python
if True and True:
    print("It's true.")
```

### `||` / `or`

Logical 'or'. Is true if at least one of the sides of the equation is true.

```python
if False or True:
    print("It's true.")
```

## Truth Tables

For easy reference when constructing compound truths.

### `&&` / `and` Truth Table

|   A   | and |   B   | ->  | Result |
|  ---  | --- |  ---  | --- |  ---   |
| true  | and | true  | ->  | true   |
| true  | and | false | ->  | false  |
| false | and | true  | ->  | false  |
| false | and | false | ->  | false  |

### `||` / `or` Truth Table

|   A   | or  |   B   | ->  | Result |
|  ---  | --- |  ---  | --- |  ---   |
| true  | or  | true  | ->  | true   |
| true  | or  | false | ->  | true   |
| false | or  | true  | ->  | true   |
| false | or  | false | ->  | false  |

[Next](https://github.com/ocoffey/Syntax-Sheets/blob/master/Python/5_Control_Flow.md "Control Flow"), we explore more methods of control flow past the `if` statement.
