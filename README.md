# C PROGRAMMING LANGUAGE
<br>

**ABOUT C**
- C is a general-purpose programming language created by Dennis Ritchie at the Bell Laboratories in 1972.
- C is strongly associated with UNIX, as it was developed to write the UNIX operating system.
- The main features of the C language include:
  - General Purpose and Portable
  - Low-level Memory Access
  - Fast Speed
  - Clean Syntax
<br>

**APPLICATION OF C**
- **Operating systems:** C is widely used for developing operating systems such as Unix, Linux, and Windows.
- **Embedded systems:** C is a popular language for developing embedded systems such as microcontrollers, microprocessors, and other electronic devices.
- **System software:** C is used for developing system software such as device drivers, compilers, and assemblers.
- **Networking:** C is widely used for developing networking applications such as web servers, network protocols, and network drivers.
- **Database systems:** C is used for developing database systems such as Oracle, MySQL, and PostgreSQL.
- **Gaming:** C is often used for developing computer games due to its ability to handle low-level hardware interactions.
- **Artificial Intelligence:** C is used for developing artificial intelligence and machine learning applications such as neural networks and deep learning algorithms.
- **Scientific applications:** C is used for developing scientific applications such as simulation software and numerical analysis tools.
- **Financial applications:** C is used for developing financial applications such as stock market analysis and trading systems.

## COMMENTS
- Comments can be used to explain code, and to make it more readable. It can also be used to prevent execution when testing alternative code.
- Comments can be singled-lined or multi-lined.
<br>

**Single-line Comments**
- Single-line comments start with two forward slashes (`//`).
- Any text between `//` and the end of the line is ignored by the compiler (will not be executed).
- EXAMPLE:
```
printf("Hello World!");    // This is a comment.
```
OUTPUT: `Hello World!`
<br>

**Multi-line Comments**
- Multi-line comments start with `/*` and ends with `*/`.
- Any text between `/*` and `*/` will be ignored by the compiler.
- EXAMPLE:
```
/* The code below,
will print the words Hello World! to the screen. */
printf("Hello World!");
```
OUTPUT: Hello World!
<br>

## VARIABLES
- Variables are containers for storing data values, like numbers and characters.
- In C, there are different types of variables (defined with different keywords), for example:
  - `int` : stores integers (whole numbers), without decimals, such as `123` or `-123`.
  - `float` : stores floating point numbers, with decimals, such as `19.99` or `-19.99`.
  - `char` : stores single characters, such as `'a'` or `'B'`. Characters are surrounded by single quotes.
<BR>

**Declaring (Creating) Variables**
<br>
- To create a variable, specify the type and assign it a value.
- Syntax:
```
type variableName = value;
```
  - EXAMPLE:
```
int myNum = 15;
```
**OR**
```
// Declare a variable
int myNum;

// Assign a value to the variable
myNum = 15;
```
**OUTPUT VARIABLES**
- **Format Specifiers**
  - Format specifiers are used together with the `printf()` function to tell the compiler what type of data the variable is storing. It is basically a placeholder for the variable value.
  - A format specifier starts with a percentage sign `%`, followed by a character.
  - For example, to output the value of an int variable, use the format specifier `%d` surrounded by double quotes (`""`), inside the `printf()` function.
  - To print other types, use %c for char and %f for float.
  - EXAMPLE:
```
// Creating variables
int myNum = 15;            // Integer (whole number)
float myFloatNum = 5.99;   // Floating point number
char myLetter = 'D';       // Character

// Print variables
printf("%d\n", myNum);
printf("%f\n", myFloatNum);
printf("%c\n", myLetter);
```
```
int myNum = 15;
char myLetter = 'D';
printf("My number is %d and my letter is %c", myNum, myLetter);
```

>[!NOTE]
>In many other programming languages (like Python, Java, and C++), you would normally use a print function to display the value of a variable. However, this is not possible in C.

|Format Specifier|Data Type|
|---|---|
|`%d` or `%i`|`int`|
|`%lu`|long unsigned int|
|`%f` or `%F`|`float`|
|`%lf`|`double`|
|`%c`|`char`|
|`s`|Used for strings (text)|

- **sizeof operator**
  - The memory size refers to how much space a type occupies in the computer's memory.
  - To actually get the size (in bytes) of a data type or variable, use the `sizeof` operator.
  - EXAMPLE:
```
int myInt;
float myFloat;
double myDouble;
char myChar;

printf("%lu\n", sizeof(myInt));
printf("%lu\n", sizeof(myFloat));
printf("%lu\n", sizeof(myDouble));
printf("%lu\n", sizeof(myChar));
```
## DATA TYPE CONVERSION
- There are two types of conversion in C:
  - Implicit Conversion (automatically)
  - Explicit Conversion (manually)
- Implicit Conversion:
  - Implicit conversion is done automatically by the compiler when you assign a value of one type to another.
- Explicit Conversion:
  - Explicit conversion is done manually by placing the type in parentheses () in front of the value.
## if loop
- **The `if` Statement**
  - Use the if statement to specify a block of code to be executed if a condition is true.
  - Syntax
```
if (condition) {
  // block of code to be executed if the condition is true
}
```
```
// EXAMPLE
if (20 > 18) {
  printf("20 is greater than 18");
}
```
- **The `else` Statement**
  - Use the else statement to specify a block of code to be executed if the condition is false.
  - Syntax:
```
if (condition) {
  // block of code to be executed if the condition is true
} else {
  // block of code to be executed if the condition is false
}
```
```
//EXAMPLE
int time = 20;
if (time < 18) {
  printf("Good day.");
} else {
  printf("Good evening.");
}
// Outputs "Good evening."
```
- **Short Hand If...Else (Ternary Operator)**
  - There is also a short-hand if else, which is known as the ternary operator because it consists of three operands.
  - It can be used to replace multiple lines of code with a single line.
  - It is often used to replace simple if else statements.
  - SYNTAX:
```
variable = (condition) ? expressionTrue : expressionFalse;
```
```
// EXAMPLE
int time = 20;
(time < 18) ? printf("Good day.") : printf("Good evening.");
```

## C-PROGRAMS
<BR>

**PROGRAM 1**
<br>
**Ques**: Printing HELLO WORLD! .
```
#include<stdio.h>
int main(){
    printf("HELLO WORLD!\n");
    return 0;
}
```
OUTPUT: HELLO WORLD!
<br>

>[!NOTE]
>Every C statement ends with a semicolon `;`
><br>
>The body of `int main()` could also been written as:
><br>
>```
>int main(){printf("Hello World!");return 0;}
>```
><br>
>The compiler ignores white spaces. However, multiple lines makes the code more readable.

<details>
  <summary> Explanation </summary>
  
- **Line1** : `#include <stdio.h>` is a header file library that lets us work with input and output functions, such as `printf()` (used in line 3). Header files add functionality to C programs.
- **Line2** : Another thing that always appear in a C program is `main()`. This is called a function. Any code inside its curly brackets `{}` will be executed.
- **Line3** : `printf()` is a function used to output/print text to the screen. In our example, it will output `"Hello World!"`.
- **Line4** : `return 0` ends the `main()` function.
- **Line 5** : Do not forget to add the closing curly bracket `}` to actually end the main function.
</details>
<br>

**PROGRAM 2**
<br>
**Ques**: Printing using newline character.
```
#include<stdio.h>
int main(){
    printf("Whatever you are,\n");
    printf("be a good one.");
    return 0;
}
```
>OUTPUT:
><br>
>Whatever you are,
><br>
>be a good one.
<br>

