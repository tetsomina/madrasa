# What Is a Programming Language?

Programming is giving a set of instructions to a computer to execute.
Programming is the mental process of thinking up instructions to give to a machine (like a computer).
Coding is the process of transforming those ideas into a written language that a computer can understand.

Programming languages are the tools we use to write instructions for computers to follow. Computers “think” in binary — strings of 1s and 0s. Programming languages allow us to translate the 1s and 0s into something that humans can understand and write. A programming language is made up of a series of symbols that serves as a bridge that allow humans to translate our thoughts into instructions computers can understand.

## Hello World

```py
my_name = "YoMama"
print("Hello and welcome " + my_name + "!")
```

## Strings

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

---

# Method

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

---

# Variable

A variable is used to store data that will be used by the program. This data can be a number, a string, a Boolean, a list or some other data type. Every variable has a name which can consist of letters, numbers, and the underscore character `_`.

The equal sign `=` is used to assign a value to a variable. After the initial assignment is made, the value of a variable can be updated to new values as needed.

## Variable Names

A variable can have a short name (like `x` and `y`) or a more descriptive name (`age`, `grade`, `grocery_list`).

Rules for Python variables:

- A variable name must start with a letter or the underscore character. It cannot start with a number.
- A variable name can only contain alpha-numeric characters and underscores (`A`-`z`, `0`-`9`, and `_`).
- Variable names are case-sensitive (`num`, `Num`, and `NUM` are three different variables).

## Variable Nomenclature

When declaring a variable in Julia, the variable name goes first, optionally followed by a type annotation and then the value.

If a variable does not need a value to be assigned immediately, it can be declared without a type and a value can be assigned later:

```pseudo
name = value # Without type annotation
name::Type = value # With type annotation
```

> **Note:** Variables in Julia are dynamic and can hold values of different types, but you can optionally declare the type for performance optimization and type-checking.

---

# Operators

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

> **Note:** Items at the same precedence are evaluated left to right. The exception to this is exponentiation, which evaluates right to left.

---

# Errors

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

The error is caused by (or at least detected at) the token preceding the arrow in the example, the error is detected at the print function, since a colon `:` is missing before it.

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

---

# Numbers

Computers can understand much more than just strings of text. Python has a few numeric data types. It has multiple ways of storing numbers. Which one you use depends on your intended purpose for the number you are saving.

An integer, or int, is a whole number. It has no decimal point and contains all counting numbers (1, 2, 3, …) as well as their negative counterparts and the number 0. If you were counting the number of people in a room, the number of jellybeans in a jar, or the number of keys on a keyboard you would likely use an integer.

A floating-point number, or a float, is a decimal number. It can be used to represent fractional quantities as well as precise measurements. If you were measuring the length of your bedroom wall, calculating the average test score of a seventh-grade class, or storing a baseball player’s batting average for the 1998 season you would likely use a float.

Numbers can be assigned to variables or used literally in a program:

```py
an_int = 2
a_float = 2.1
print(an_int + 3)
```

---

# Data Types

'Python is a strongly typed language. At runtime, it prevents typing errors and engages in little implicit type conversion.'

Python is a strongly typed language, in the sense that at runtime it prevents typing errors and it engages in little implicit type conversion or casting, i.e. converting one type to another without a specific call to a conversion function.

```py
address = 575
address = "575 broadway"
```

After line 1, `address` is an `int`. After line 2, `address` is a `str`.

Python includes the following categories of built-in data types:

- String type: `str`
- Boolean type: `bool`
- Binary types: `bytes`, `bytearray`, `memoryview`
- Number types: `int`, `float`, `complex`
- Sequence Types: `list`, `range`, `tuple`
- Set types: `set`, `frozenset`
- Dictionary type: `dict`

## type()

The `type()` function can be used to retrieve the data type of an object:

```py
message = "Hello, world!"

print(type(message))
# Output: <class 'str'>
```

## isinstance()

The `isinstance()` function can be used to test if an object is an instance of a specified type. This will print a boolean value for each function call, indicating if the object is an instance of the given type:

```py
word = "purple"
languages = ("Python", "C++", "Go")

print(isinstance(word, str)) # Output: True
print(isinstance(languages, list)) # Output: False
print(isinstance(languages, tuple)) # Output: True
```

# Casting

Casting, also known as type conversion, is a process that converts a variable's data type into another data type. These conversions can be implicit (automatically interpreted) or explicit (using built-in functions).

## Implicit Type Conversion

The Python interpreter automatically performs type conversion on some operations without any user involvement.

Python avoids data loss by converting lower data types to higher data types. For example, an integer, 7, is converted to a float when added with another float, 2.2:

```py
y = 7 + 2.2
# Python automatically type casts y into float

print(y)
# Output: 9.2

print(type(y))
# Output: <class 'float'>
```

Since the expression above represents the sum of two `float` values, the data type of `y` is also a `float`.

## Explicit Type Conversion

Explicit type casting involves Python's predefined functions that act as a constructor of another data type:

- The `str()` function takes an integer or float as an argument and converts it to a string.
- The `int()` function takes a string or float as an argument converts it to an integer.
- The `float()` function takes an integer or string as an argument and converts it to a float.

## Operations on Different Types of Data

When operating on data, it is important to be mindful of the data types associated with it. The following code is a flawed attempt to print the square of a number specified by the user. When run, a `TypeError` will be thrown:

```py
num = input("Please enter a number: ")
print(num ** 2)
```

The `input()` function takes input from the user and stores it in a variable as a string. However, the `**` operator takes two numbers and returns the first number to the power of the second. In order to make the code work, the input variable must be cast to a number type.

---

# Calculations

Computers absolutely excel at performing calculations. The “compute” in their name comes from their historical association with providing answers to mathematical questions. Python performs the arithmetic operations of addition, subtraction, multiplication, and division with `+`, `-`, `*`, and `/`.

```py
# Prints "500"
print(573 - 74 + 1)

# Prints "50"
print(25 * 2)

# Prints "2.0"
print(10 / 5)
```

The result has a decimal place. This is because Python converts all ints to floats before performing division. Division can throw its own special error: `ZeroDivisionError`. Python will raise this error when attempting to divide by 0.

### Operators

Operators are used to perform various operations on variables and values. The standard arithmetic and assignment operators are the most familiar.

### Syntax

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

> **Note:** Items at the same precedence are evaluated left to right. The exception to this is exponentiation, which evaluates right to left.

# Changing Numbers

Variables that are assigned numeric values can be treated the same as the numbers themselves. Two variables can be added together, divided by `2`, and multiplied by a third variable without Python distinguishing between the variables and _literals_ (like the number `2` in this example). Performing arithmetic on variables does not change the variable — you can only update a variable using the `=` sign.

```py
coffee_price = 1.50
number_of_coffees = 4

# Prints "6.0"
print(coffee_price * number_of_coffees)
# Prints "1.5"
print(coffee_price)
# Prints "4"
print(number_of_coffees)

# Updating the price
coffee_price = 2.00

# Prints "8.0"
print(coffee_price * number_of_coffees)
# Prints "2.0"
print(coffee_price)
# Prints "4"
print(number_of_coffees)
```

We create two variables and assign numeric values to them. Then we perform a calculation on them. This doesn’t update the variables! When we update the `coffee_price` variable and perform the calculations again, they use the updated values for the variable!

# Exponents

Python can also perform exponentiation. In written math, you might see an exponent as a superscript number, but typing superscript numbers isn’t always easy on modern keyboards. Since this operation is so related to multiplication, we use the notation `**`.

```py
# 2 to the 10th power, or 1024
print(2 ** 10)

# 8 squared, or 64
print(8 ** 2)

# 9 * 9 * 9, 9 cubed, or 729
print(9 ** 3)

# Perform fractional exponents
# 4 to the half power, or 2
print(4 ** 0.5)
```

# Modulo

Python offers a companion to the division operator called the modulo operator. The modulo operator is indicated by `%` and gives the remainder of a division calculation. If the two numbers are divisible, then the result of the modulo operation will be 0.

**Modulo** is a mathematical operation that returns the remainder of a division of two arguments.

### Syntax

The remainder is what is left over after dividing the first argument, the dividend, by the second, the divisor or modulus:

```pseudo
remainder = dividend % divisor
```

Most programming languages use the `%` symbol to represent the modulo operation, though some may use `mod` or other variations.

### Example

```pseudo
# Prints 4 because 29 / 5 is 5 with a remainder of 4
print(29 % 5)

# Prints 2 because 32 / 3 is 10 with a remainder of 2
print(32 % 3)

# Modulo by 2 returns 0 for even numbers and 1 for odd numbers
# Prints 0
print(44 % 2)
```

The modulo operator used to find the remainder of division operations. `29 % 5` equals 4, `32 % 3` equals 2, and `44 % 2` equals 0.

```pseudo
print(3 % 3) # Prints 0
print(4 % 3) # Prints 1
print(5 % 3) # Prints 2
print(6 % 3) # Prints 0
print(7 % 3) # Prints 1
```

In each of these modulo operations, 3 is the divisor. Since `3 / 3` equals 1 with no remainder, the result of the first modulo operation is 0. Note that as the dividend increases by 1, the remainder also increases by 1, until we reach the next number that is evenly divisible by 3 — this creates a pattern that repeats contiuously as the dividend increases by 1

Because of this, the modulo operator is useful in programming when we want to perform an action every nth time something occurs. Imagine you own a small café and would like for every 7th customer to receive a survey. If every customer transaction is numbered in the order they occur, you can determine which customers should receive the survey by calculating `<transaction number> % 7` — if the result is 0, hand out the survey!

# Transaction

A **transaction** is an encapsulated set of instructions sent to a database that must happen as a unit. If something interrupts the transaction, such as an error, none of the instructions in the transaction occur. This ensures that there are never any partially executed transactions.

Transactions are used to preserve the consistency of a database, so that execution of a complex process, such as debiting one account and crediting another, is never partially completed. In the prior example, without transactions, an error or a resource lock could leave the first account debited without making the corresponding credit. Transactions adhere to **ACID properties** in order to ensure this doesn’t happen.
