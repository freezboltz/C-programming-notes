## Hello World

To create a simple C program which prints "Hello, World" on the screen, use a text editor to create a new file (e.g. hello.c -- the file extension must be .c) containing the following source code:

##### hello.c
```
#include <stdio.h>

int main(void)
{
    puts("Hello, World");
    return 0;
}
```
#### Let's look at this simple program line by line

```#include <stdio.h>```

This line tells the compiler to include the contents of the standard library header file stdio.h in the program.
Headers are usually files containing function declarations, macros and data types, and you must include the header file
before you use them. This line includes stdio.h so it can call the function puts().

```int main(void)```

This line starts the definition of the function. It states the name of the function (main), the type and number of
arguments it expects(void, meaning none), and the type of value that this function returns (int). Program execution starts
in the main() function.

```
{
    ...
}
```
The curly braces are used in pairs to indicate where a block of code begins and ends. They can be used in a lot of ways, but
in this case they indicate where the function begins and ends.

```puts("Hello, World");
```

This line calls the puts() function to output text to standard output(the screen, by default), followed by a newline.

Compile this code using gcc compiler

#### Executing the program

Once compiled, the binary file may then be executed by typing ./hello in the terminal. Upon execution, the compiled program
will print Hello, World, followed by a newline, to the command prompt.
