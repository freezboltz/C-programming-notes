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

```
#include <stdio.h>
```

This line tells the compiler to include the contents of the standard library header file stdio.h in the program.
Headers are usually files containing function declarations, macros and data types, and you must include the header file
before you use them. This line includes stdio.h so it can call the function puts().

```
int main(void)
```

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

```
puts("Hello, World");
```

This line calls the puts() function to output text to standard output(the screen, by default), followed by a newline.

The string to be output is included within the parenthesis.

"Hello, World" is the string that will be written to the screen. In C, every string literal value must be inside the
double quotes "...".

In C programs, every statement needs to be terminated by a semi-colon (i.e. ;).

```
return 0;
```

When we define main(), we declared it as a function returning an int, meaning it needs to return an integer.
In this example, we are returning the integer value 0, which is used to indicate that the program exited successfully.
After the retur 0; statement, the execution process will terminate.

#### Editing the program

Simple text editor include vim or gedit on Linux, or Notepad on Windows. Cross-platform editors also include VScode.

The editor must create plain text files, not RTF or any other format.

#### Compling and running the program

To run the program, this source file (hello.c) first needs to be compiled into an executable file (e.g. hello on
Unix/Linux system or hello.exe on Windows). This is done using a complier for the C language.

#### Compile using GCC

GCC (GNU Compiler Collection) is a widely used C compiler. To use it, open a terminal, use the command line to
navigate to the source file's location and then run:

```
gcc hello.c -o hello
```

If no errors are found in the source code (hello.c), the compiler will create a binary file, the name of which is given
by the argument to the -o flag in command line option (hello). This is the final executable file.

We can also use the warning options -Wall -Wextra -Werror, that help to identify problems that can cause the program to fail
or produce unexpected results. They are not necessary for this simple program but this is way of adding them:

```
gcc -Wall -Wextra -Werror -o hello hello.c
```

#### Using the clang compiler

To compile the program using clang you can use:

```
clang -Wall -Wextra -Werror -o hello hello.c
```

By design, the clang command line option are similer to those of GCC.

Compile this code using gcc compiler

#### Executing the program

Once compiled, the binary file may then be executed by typing ./hello in the terminal. Upon execution, the compiled program
will print Hello, World, followed by a newline, to the command prompt.
