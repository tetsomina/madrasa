Title: 'What Is a Programming Language?'

Programming is giving a set of instructions to a computer to execute.
Programming is the mental process of thinking up instructions to give to a machine (like a computer).
Coding is the process of transforming those ideas into a written language that a computer can understand.

Programming languages are the tools we use to write instructions for computers to follow. Computers “think” in binary — strings of 1s and 0s. Programming languages allow us to translate the 1s and 0s into something that humans can understand and write. A programming language is made up of a series of symbols that serves as a bridge that allow humans to translate our thoughts into instructions computers can understand.

##### Hello World
`python
my_name = "YoMama"
print("Hello and welcome " + my_name + "!")`

Title: 'Strings'

Computer programmers refer to blocks of text as strings. In computer science, sequences of characters are referred to as strings. A string is a sequence of characters contained within a pair of single quotes (') or double quotes("). Strings can store words, sentences, or whole paragraphs. Strings can be any length and can include any character such as:
    Letters
    Numbers
    Symbols
    Whitespace (spaces, tabs, new lines)

They are usually contained within a pair of 'single quotes' or "double quotes".

Like any other list, each character in a string has an **index** that denotes a character’s position.

It is possible to concatenate strings together using + in some languages, such as Python and C++.

```py
block_number = "555"
street_name = "Madison Ave"
address = block_number + ' ' + street_name
print(address)
```



#### How can I use quotes inside of a string?
Vary your use of single quotes vs double quotes:

```py
print(‘Then there he stood, surveying the crop fields before saying “We have an infestation”’)
```

Another way to use special character inside strings is to use the sequence escape character backslash(\).

```py
print(“Then there he stood, surveying the crop fields before saying \“We have an infestation\””)
```

Title: 'Method'

**Methods** are the "behavior" part of the class. When an instance variable is created from a class, it has access to the class's associated methods. Methods can accept parameters (sometimes they're called "arguments") and can return a result.

In object-oriented programming, methods promote reusability and keep functionality encapsulated inside an object.

Classes can be broken into two core parts:

- The data that is attributed to a class's members or properties.
- The behaviors that are defined or inherited in the class.

## Example

In the Python example below, a class for a character in a game, `Character`, is defined with certain behaviors. The character can:

- Introduce themselves via `.introduceSelf()`.
- Move left given an integer amount via `.moveLeft()`.
- Move right given an integer amount via `.moveRight()`.

```py
class Character:
  def __init__(self, name, movex):
    self.name = "Player"  # Character's name
    self.movex = 0        # Character's starting position

  def introduceSelf(self):
    # Print out an introduction phrase
    print(f"Hello! I'm {self.name}.")

  def moveLeft(self, x):
    # Move the character left by x pixels
    self.movex -= x

  def moveRight(self, x):
    # Move the character right by x pixels
    self.movex += x
```


Title: 'Variable'

A variable is used to store data that will be used by the program. This data can be a number, a string, a Boolean, a list or some other data type. Every variable has a name which can consist of letters, numbers, and the underscore character ```_```.

The equal sign ```=``` is used to assign a value to a variable. After the initial assignment is made, the value of a variable can be updated to new values as needed.

## Variable Names

A variable can have a short name (like `x` and `y`) or a more descriptive name (`age`, `grade`, `grocery_list`).

Rules for Python variables:

- A variable name must start with a letter or the underscore character. It cannot start with a number.
- A variable name can only contain alpha-numeric characters and underscores (`A`-`z`, `0`-`9`, and `_`).
- Variable names are case-sensitive (`num`, `Num`, and `NUM` are three different variables).

Title: 'Operators'

Operators are used to perform various operations on variables and values. The standard arithmetic and assignment operators are the most familiar.

## Syntax

The following code snippet uses the assignment operator, `=`, to set `my_variable` to the value of `num1` and `num2` with an arithmetic operator acting on them. For example, if `operator` represented `*`, `my_variable` would be assigned a value of `num1 * num2`.

```pseudo
my_variable = num1 operator num2
```

Python operators can be organized into the following groups:

- Arithmetic operators for performing traditional math evaluations.
- Assignment operators for assigning values to variables.
- Comparison operators for comparing two values.
- Logical operators for combining boolean values.

## Arithmetic Operators

Python has the following arithmetic operators:

- Addition, `+`, which returns the sum of two numbers.
- Subtraction, `-`, which returns the difference of two numbers.
- Multiplication, `*`, which returns the product of two numbers.
- Division, `/`, which returns the quotient of two numbers.
- Exponentiation, `**`, which returns the value of one number raised to the power of another.
- Modulus, `%`, which returns the remainder of one number divided by another.
- Floor division, `//`, which returns the integer quotient of two numbers.

## Assignment Operators

Python includes the following assignment operators:

- The `=` operator assigns the value on the right to the variable on the left.
- The `+=` operator updates a variable by incrementing its value and reassigning it.
- The `-=` operator updates a variable by decrementing its value and reassigning it.
- The `*=` operator updates a variable by multiplying its value and reassigning it.
- The `/=` operator updates a variable by dividing its value and reassigning it.
- The `%=` operator updates a variable by calculating its modulus against another value and reassigning it.

## Comparison Operators

Python has the following comparison operators:

- Equal, `==`, for returning `True` if two values are equal.
- Not equal, `!=`, for returning `True` if two values are not equal.
- Less than, `<`, for returning `True` if left value less than right value.
- Less than or equal to, `<=`, for returning `True` if left value is less than or equal to right value.
- Greater than, `>`, for returning `True` if left value greater than right value.
- Greater than or equal to, `>=`, for returning `True` if left value greater than or equal to right value.

## Logical Operators

Python has the following logical operators:

- The `and` operator returns `True` if both statements are `True`.
- The `or` operator returns `True` if either statement is `True`.
- The `not` operator returns `True` if its associated statement is `False`.

## Order of Operations

Python evaluates an expression in order of precedence as follows:

- Items in parentheses, (`(`...`)`), have the highest level of precedence, expressions within them are evaluated first.
- Exponentiation (`**`)
- Multiplication and division operators (`*`, `/`, `//` & `%`)
- Addition and subtraction (`+` & `-`)
- Comparison (`<`, `<=`, `>` & `>=`)
- Equality (`==` & `!=`)
- `not`
- `and`
- `or`

## Membership operators

- The `in` operator returns `True` if the element on the left is found within the iterable object on the right. Here, the element on the right side of the `in` operator must be an iterable object like a list, string, dictionary, etc.
- The `not in` operator returns `False` if the element on the left is not found within the iterable object on the right. Again, the element on the right side of the `not in` operator must be an iterable object.

**Note:** Items at the same precedence are evaluated left to right. The exception to this is exponentiation, which evaluates right to left.

Title: 'Errors'

Humans are prone to making mistakes. Humans are also typically in charge of creating computer programs. To compensate, programming languages attempt to understand and explain mistakes made in their programs.

Python refers to these mistakes as errors and will point to the location where an error occurred with a ^ character. When programs throw errors that we didn’t expect to encounter we call those errors bugs. Programmers call the process of updating the program so that it no longer produces unexpected errors debugging.

Two common errors that we encounter while writing Python are SyntaxError and NameError.

- `SyntaxError` means there is something wrong with the way your program is written — punctuation that does not belong, a command where it is not expected, or a missing parenthesis can all trigger a SyntaxError.

- A `NameError` occurs when the Python interpreter sees a word it does not recognize. Code that contains something that looks like a variable but was never defined will throw a NameError.


The two types of **errors** in Python are syntax errors and exceptions.

## Syntax Errors

Syntax errors (also known as parsing errors) occur when a sequence of characters, or tokens, violates the syntax of the Python programming language:

```shell
File "script.py", line 1
  while True print("Hello world!")
                   ^
SyntaxError: invalid syntax
```

The parser repeats the offending line and displays a little arrow `^` pointing at the earliest point in the line where the error was detected.

The error is caused by (or at least detected at) the token preceding the arrow in the example, the error is detected at the [`print()`](https://www.codecademy.com/resources/docs/python/built-in-functions/print) function, since a colon `:` is missing before it.

File name and line number are printed to state where the error originated.

## Exceptions

Even if a statement or expression is syntactically correct, it may cause an error when an attempt is made to execute it. Errors detected during execution are called exceptions and are not unconditionally fatal. Most exceptions are not handled by programs, however, and result in error messages as shown here:

### Value Error

`ValueError` is thrown when a function's argument is of the correct type, but an inappropriate value, such as being out of range.

```shell
Traceback (most recent call last):
File "script.py", line 1, in <module>
int('xyz')
ValueError: invalid literal for int() with base 10: 'xyz'
```

### Name Error

`NameError` is thrown when an object could not be found.

```shell
Traceback (most recent call last):
File "script.py", line 1, in <module>
age
NameError: name 'age' is not defined
```

### Index Error

`IndexError` is thrown when trying to access an item at an invalid index.

```shell
Traceback (most recent call last):
File "script.py", line 1, in <module>
employees[3]
IndexError: list index out of range
```

### Module Not Found Error

`ModuleNotFoundError` is thrown when a module could not be found.

```shell
Traceback (most recent call last):
File "script.py", line 1, in <module>
import notamodule
ModuleNotFoundError: No module named 'notamodule'
```

### Type Error

`TypeError` is thrown when a function's argument is of an inappropriate type.

```shell
Traceback (most recent call last):
File "script.py", line 1, in <module>
max(True)
TypeError: 'bool' object is not iterable
```

### Zero Division Error

`ZeroDivisionError` is thrown when the second operator in the division is zero.

```shell
Traceback (most recent call last):
File "script.py", line 1, in <module>
ratio = 100 / 0
ZeroDivisionError: division by zero
```
