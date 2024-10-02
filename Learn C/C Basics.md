#   The C Programming Language

C is an older language compared to other languages in use and yet it is still very popular. The **[TIOBE Index](https://www.tiobe.com/tiobe-index/)**, which measures the popularity of programming languages, has C at the top of the list for many years. This is due to C’s use in all areas of computing.

Most operating systems today including the Linux Kernel are implemented with C code. The main version of the Python programming language is named CPython because it is implemented using C. C has also been extended using the languages C++ and C#.

C is also common in embedded systems which are smaller computing units that control things like home appliances, lighting controllers, and other small physical devices.

The C programming language is everywhere. Learning it will help you become a better programmer ready for the next challenge in any field of computer science.

##  Hello World

```c
#include <stdio.h>

int main() {
  // output a line
  printf("Hello World!\n");
}
```

Line explanation:

-   `#include <stdio.h>`: This line is needed to run the line of code that starts with `printf`.
-   `int main(){ }`: This is the starting point of the code. All the code inside the curly braces `{}` runs first.
-   `// output a line`: This is a comment. It is not a line of code but a message we can add to code to tell ourselves or others what the code does. When the code is run this line will be ignored.
-   `printf("Hello World!")`;: This line of code prints, or outputs, the text “Hello World!” to the console. Printing text to the console is one way for a program to communicate with the user.

##  Syntax and Errors

### Case Sensitivity

Most of the words in the code use all lowercase letters. This is known as case-sensitivity. Whether lowercase or uppercase, certain words in the code must follow the correct case in order for the code to run. The only lines of text that can change case are the comment and the text between quotes.

### The Semicolon

All statements, like the `printf()` statement, need to end with a semicolon. This identifies the end of the statement and is needed for the code to run correctly.

### Double Quotes

The text in between the double quotes " is known as a string (think of a string of characters). All **strings** must be surrounded by double-quotes.



