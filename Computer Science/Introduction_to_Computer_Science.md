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

In python, a string is a sequence of characters contained within a pair of single quotes (`'`) or double quotes(`"`). Strings can store words, sentences, or whole paragraphs. They can be any length and can contain letters, numbers, symbols, and spaces.

```py
message1 = "I am a string"
message2 = 'I am also a string'
```

Like any other list, each character in a string has an **index** that denotes a character’s position.

It is possible to concatenate strings together using + in some languages, such as Python and C++.

```py
block_number = "555"
street_name = "Madison Ave"
address = block_number + ' ' + street_name
print(address)
```

Strings are immutable; they cannot change. Every time an operation is performed on a string, a new string is created in memory.

## Accessing the Characters of a String

Strings in Python are technically a type of `[list]` — one in which each character is a separate element. This means each character in a string can be individually accessed by index, like with the elements in a list:

```py
myString = "Hello, World!"

var_1 = myString[0]
var_2 = myString[7:]
var_3 = myString[1:4]

print("var_1: " + var_1) # Output: var_1: H
print("var_2: " + var_2) # Output: var_2: World!
print("var_3: " + var_3) # Output: var_3: ell
```

If an attempt is made to access an index out of bounds, it will return an `IndexError`.

```py
name = "phillis"
name[8] # Throws an IndexError
```

## Multi-line Strings

Strings can be long or short. For longer text, a multi-line string can be used. Multi-line strings begin and end with three single or double quotes:

```py
my_string = """If it were done when 'tis done, then 'twere well
It were done quickly: if the assassination
Could trammel up the consequence, and catch
With his surcease success; that but this blow
Might be the be-all and the end-all here,
But here, upon this bank and shoal of time,
We'ld jump the life to come."""
```

## Escape Characters

Sometimes a string may have a character that Python tries to interpret, such as `'`.

```py
my_string = 'It's a lovely day!'

print(my_string)
```

This will raise an error, because the interpreter thinks the second `'` marks the end of the string.

```shell
  File "main.py", line 1
    my_string = 'It's a lovely day!'
                    ^
SyntaxError: invalid syntax
```

These characters can be "escaped" by adding a backslash beforehand. The `\` is called an escape character.

The backslash will not be visible if the string is printed:

```py
my_string = 'It\'s a lovely day!'

print(my_string)
# Output: It's a lovely day!
```

This problem can be avoided by wrapping strings containing `'` characters in double quotes:

```py
my_string = "It's a lovely day!"

print(my_string)
# Output: It's a lovely day!
```

Python also has a series of non-printing characters that can modify strings. For example, `\n` adds a new line and `\t` adds a tab:

```py
note = "I am on top!\nI am on bottom. \n\tI am indented!"

print(note)
```

This will output:

```shell
I am on top!
I am on bottom.
        I am indented!
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

Transactions are used to preserve the consistency of a database, so that execution of a complex process, such as debiting one account and crediting another, is never partially completed. Without transactions, an error or a resource lock could leave the first account debited without making the corresponding credit. Transactions adhere to **ACID properties** in order to ensure this doesn’t happen.

---

# Concatenation

The `+` operator doesn’t just add two numbers, it can also “add” two strings! The process of combining two strings is called _string concatenation_. Performing string concatenation creates a brand new string comprised of the first string’s contents followed by the second string’s contents (without any added space in-between).

```py
greeting_text = "Hey there!"
question_text = "How are you doing?"
full_text = greeting_text + question_text

# Prints "Hey there!How are you doing?"
print(full_text)
```

In this sample of code, we create two variables that hold strings and then concatenate them. But we notice that the result was missing a space between the two, let’s add the space in-between using the same concatenation operator!

```py
full_text = greeting_text + " " + question_text

# Prints "Hey there! How are you doing?"
print(full_text)
```

Now the code prints the message we expected.

If you want to concatenate a string with a number you will need to make the number a string first, using the `str()` function. If you’re trying to `print()` a numeric variable you can use commas to pass it as a different argument rather than converting it to a string.

```py
birthday_string = "I am "
age = 10
birthday_string_2 = " years old today!"

# Concatenating an integer with strings is possible if we turn the integer into a string first
full_birthday_string = birthday_string + str(age) + birthday_string_2

# Prints "I am 10 years old today!"
print(full_birthday_string)

# If we just want to print an integer
# we can pass a variable as an argument to
# print() regardless of whether
# it is a string.

# This also prints "I am 10 years old today!"
print(birthday_string, age, birthday_string_2)
```

Using `str()` we can convert variables that are not strings to strings and then concatenate them. But we don’t need to convert a number to a string for it to be an argument to a print statement.

---

# Plus Equals

Python offers a shorthand for updating variables. When you have a number saved in a variable and want to add to the current value of the variable, you can use the `+=` (plus-equals) operator.

```py
# First we have a variable with a number saved
number_of_miles_hiked = 12

# Then we need to update that variable
# Let's say we hike another two miles today
number_of_miles_hiked += 2

# The new value is the old value
# Plus the number after the plus-equals
print(number_of_miles_hiked)
# Prints 14
```

Above, we keep a running count of the number of miles a person has gone hiking over time. Instead of recalculating from the start, we keep a grand total and update it when we’ve gone hiking further.

The plus-equals operator also can be used for string concatenation, like so:

hike_caption = "What an amazing time to walk through nature!"

```py
# Almost forgot the hashtags!
hike_caption += " #nofilter"
hike_caption += " #blessed"
```

We create the social media caption for the photograph of nature we took on our hike, but then update the caption to include important social media tags we almost forgot.

# Multi-line Strings

Python strings are very flexible, but if we try to create a string that occupies multiple lines we find ourselves face-to-face with a `SyntaxError`. Python offers a solution: _multi-line strings_. By using three quote-marks (`"""` or `'''`) instead of one, we tell the program that the string doesn’t end until the next triple-quote. This method is useful if the string being defined contains a lot of quotation marks and we want to be sure we don’t close it prematurely.

```pseudo
leaves_of_grass = """
Poets to come! orators, singers, musicians to come!
Not to-day is to justify me and answer what I am for,
But you, a new brood, native, athletic, continental, greater than
  before known,
Arouse! for you must justify me.
"""
```

In the above example, we assign a famous poet’s words to a variable. Even though the quote contains multiple linebreaks, the code works!

If a multi-line string isn’t assigned a variable or used in an expression it is treated as a comment.

---

# Comment

A **comment** is a note or explanation in the source code of a computer program. They are added with the purpose of making the code easier for ourselves or other developers to understand in the future, and they are generally ignored by compilers and interpreters.

Comments are typically formatted as either:

- Single-line comments, which start with a comment delimiter and continue until the end of the line.
- Multi-line comments, which start with a start delimiter and end with an end delimiter and can span multiple lines.

Some programming languages support only one type of comment. For example, Python comments are single-line comments: They start with `#` and continue to the end of the line.

Other languages employ both single-line and multi-line comments. For example, C and C++ have single-line comments that start with `//` and multi-line comments between `/*` and `*/` that can span multiple lines.

## Uses

How best to make use of comments is subject to dispute. Here are some common ways comments are used:

### Code Description

Comments can be used to summarize code or to explain the programmer's intent. They can provide additional information to aid in understanding the code.

### Debugging

When an error is encountered in the program, a common debugging practice is to comment out some code, meaning to add comment syntax causing that block of code to become a comment, so that it will not be executed in the program. This may be done to exclude certain pieces of code from the program.

By strategically commenting out and running only parts of the program, the source of the error can be determined through process of elimination.

### Metadata

Comments in a computer program often store metadata about a program file.

Other metadata includes:

- The name of the creator of the original version of the program file
- The date when the first version was created
- The names of other people who have edited the program file so far
- The URL of documentation about how to use the program
- The name of the software license for the program file

---

## Project: Block Letters

ASCII art is a graphic design technique that uses computers for presentation and consists of pictures pieced together from individual characters.

Write a Python program called initials.py that displays the initials of your name in block letters.

```py
print("JJJJJ    A  ")
print("  J     A A ")
print("  J    A   A")
print("  J    AAAAA")
print("J J    A   A")
print("J J    A   A")
print("JJJ    A   A")
```

## Project: Receipts for Lovely Loveseats

We’ve decided to pursue the dream of small-business ownership and open up a furniture store called Lovely Loveseats for Neat Suites on Fleet Street. With our newfound knowledge of Python programming, we’re going to build a system to help speed up the process of creating receipts for your customers.

```py
lovely_loveseat_description = "Lovely Loveseat.Tufted polyester blend on wood. 32 inches high x 40 inches wide x 30 inches deep. Red or white."
lovely_loveseat_price = 254.00

stylish_settee_description = "Stylish Settee. Faux leather on birch. 29.50 inches high x 54.75 inches wide x 28 inches deep. Black."
stylish_settee_price = 180.50

luxurious_lamp_description = "Luxurious Lamp. Glass and iron. 36 inches tall. Brown with cream shade."
luxurious_lamp_price  = 52.15

sales_tax = 0.088

customer_one_total  = 0
customer_one_itemization  = ""

customer_one_total += lovely_loveseat_price
customer_one_itemization += lovely_loveseat_description

customer_one_total += luxurious_lamp_price
customer_one_itemization += luxurious_lamp_description

customer_one_tax  = customer_one_total * sales_tax
customer_one_total  += customer_one_tax

print("Customer One Items:")
print(customer_one_itemization)
print("Customer One Total:")
print(customer_one_total)

customer_two_total  = 0
customer_two_itemization  = ""

customer_two_total += stylish_settee_price
customer_two_itemization  +=  stylish_settee_description

print("")

customer_two_total += luxurious_lamp_price
customer_two_itemization += luxurious_lamp_description

customer_two_tax  = customer_two_total * sales_tax
customer_two_total  += customer_two_tax

print("Customer Two Items:")
print(customer_two_itemization)
print("Customer Two Total:")
print(customer_two_total)
```

---

# Introduction to Control Flow

Imagine waking up in the morning.

You wake up and think, “Ugh. Is it a weekday?”

If so, you have to get up and get dressed and get ready for work or school. If not, you can sleep in a bit longer and catch a couple extra Z’s. But alas, it is a weekday, so you are up and dressed and you go to look outside, “What’s the weather like? Do I need an umbrella?”

These questions and decisions control the flow of your morning, each step and result is a product of the conditions of the day and your surroundings. Your computer, just like you, goes through a similar flow every time it executes code. A program will run (wake up) and start moving through its checklists, is this condition met, is that condition met, okay let’s execute this code and return that value.

This is the _control flow_ of your program. In Python, your script will execute from the top down, until there is nothing left to run. It is your job to include gateways, known as conditional statements, to tell the computer when it should execute certain blocks of code. If these conditions are met, then run this function.

In summary, **Control flow** refers to the order in which statements and instructions are executed in a program. It determines how the program progresses from one instruction to another based on certain conditions and logic. Control flow mechanisms allow developers to create dynamic and flexible programs that can make decisions, repeat tasks, and respond to various inputs.

## Ways To Control Flow in a Program

### 1. Conditional Statements

Conditional statements provide the ability to make decisions within a program based on certain conditions. They typically use boolean expressions to determine whether a particular block of code should be executed or skipped. The most common conditional statements are:

- **If Statements:** An `if` statement evaluates a condition and executes a block of code if the condition is true. It can be followed by optional `else-if` and `else` clauses to handle alternative conditions.

- **Switch Statements:** A `switch` statement allows the program to choose between multiple alternatives based on the value of an expression. It compares the expression with various cases and executes the code block associated with the first matching case.

### 2. Loops

Loops are used to repeat a block of code multiple times until a certain condition is met. They are handy for iterating over collections, performing repetitive tasks, and implementing algorithms that require repeated execution. The following types of loops are commonly used:

- **For Loops:** A `for` loop executes a block of code a fixed number of times, typically iterating over a range of values. It typically consists of an initialization statement, a condition for termination, and an increment or decrement statement.

- **While Loops:** A `while` loop repeatedly executes a block of code as long as a specified condition remains true. It evaluates the condition before each iteration, and if the condition becomes false, the loop is terminated.

- **Do-While Loops:** A `do-while` loop is similar to a `while` loop but guarantees that the code block is executed at least once. It evaluates the condition after executing the block, and if the condition is true, the loop continues.

### 3. Control Flow Keywords

Many programming languages provide control flow keywords or constructs that alter the normal flow of program execution. These keywords enable developers to perform specific actions such as early termination, branching, or jumping to a different part of the program. Some commonly used control flow keywords include:

- **Break:** The `break` keyword is used to exit a loop or switch statement prematurely. It terminates the innermost loop or immediately exits the switch statement.

- **Continue:** The `continue` keyword is used within a loop to skip the remaining statements in the current iteration and move to the next iteration.

- **Return:** The `return` keyword is used to exit a function or method and return a value to the caller. It can also be used to terminate the execution of a program in some cases.

## Conditionals

Conditionals take an expression, which is code that evaluates to determine a value, and checks if it is `True` or `False`. If it’s `True`, we can tell our program to do one thing — we can even account for `False` to do another.

As we write more complex programs, conditionals allow us to address multiple scenarios and make our programs more robust.

## If Statement

The Python `if` statement is used to determine the execution of code based on the evaluation of a Boolean expression.

- If the `if` statement expression evaluates to `True`, then the indented code following the statement is executed.
- If the expression evaluates to `False` then the indented code following the if statement is skipped and the program executes the next line of code which is indented at the same level as the if statement.

```py
test_value = 100

if test_value > 1:
  print("This code is executed!")

if test_value > 1000:
  print("This code is NOT executed!")

print("Program continues at this point.")
```

## Else Statement

The Python `else` statement provides alternate code to execute if the expression in an if statement evaluates to `False`.

The indented code for the `if` statement is executed if the expression evaluates to `True`. The indented code immediately following the `else` is executed if and only if the expression evaluates to `False`.

To mark the end of the else block, the code must be unindented to the same level as the starting if line.

```py
test_grade = 61

if test_grade > 60:
  print("You passed.")
else:
  print("You failed.")

# Output: You passed.
```

## Elif Statement

The Python `elif` statement allows for continued checks to be performed after an initial `if` statement. An `elif` statement differs from the else statement because another expression is provided to be checked, just as with the initial `if` statement.

If the expression is `True`, the indented code following the `elif` is executed. If the expression evaluates to False, the code can continue to an optional `else` statement.

Multiple elif statements can be used following an initial `if` to perform a series of checks. Once an `elif` expression evaluates to `True`, no further `elif` statements are executed.

```py
pet_type = "fish"

if pet_type == "dog":
  print("You have a dog.")
elif pet_type == "cat":
  print("You have a cat.")
elif pet_type == "fish":
  # This is performed
  print("You have a fish")
else:
  print("Not sure!")
```

## Boolean

A **boolean** holds a true or false value and are mostly used in conditional statements to control a program's flow of execution. This data type is named after George Boole, a 19th century English logician.

Some languages use comparison operators such as:

- `>=` and `<=`, for "greater than" and "less than", respectively.
- `==` and `is` or `!=` and `not` to test for equality and inequality, respectively.

Other languages may use a combination of "falsy" values (e.g. `""`, `null`, or `0`) and "truthy" values such as `1`.

### Boolean Operators

Often, the conditions you want to check in your conditional statement will require more than one boolean expression to cover. In these cases, you can build larger boolean expressions using boolean operators. These operators (also known as logical operators) combine smaller boolean expressions into larger boolean expressions.

There are three boolean operators that we will cover:

- and
- or
- not

---

# Relational Operators: Equals and Not Equals

In python, we can create a boolean expression by using relational operators.

Relational operators compare two items and return either `True` or `False`. For this reason, you will sometimes hear them called _comparators_.

The relational operators python has are:

- Equals: `==`
- Not equals: `!=`
- `>` greater than
- `>=` greater than or equal to
- `<` less than
- `<=` less than or equal to

These operators compare two items and return `True` or `False` if they are equal or not.

We can create boolean expressions by comparing two values using these operators:

```py
1 == 1     # True

2 != 4     # True

3 == 5     # False

'7' == 7   # False
```

Each of these is an example of a boolean expression.

The `''` marks in `'7'` make it a string, which is different from the integer value 7, so they are not equal. When using relational operators it is important to always be mindful of type.

```py
my_baby_bool = "true"

type(my_baby_bool)

print(type(my_baby_bool))

my_baby_bool_two = True
type(my_baby_bool_two)

print(type(my_baby_bool_two))
```
