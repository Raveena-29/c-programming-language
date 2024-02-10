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
|`%s`|Used for strings (text)|

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
- **The `else if` statement**
  - Use the else if statement to specify a new condition if the first condition is false.
  - Syntax:
```
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}
```
```
int time = 22;
if (time < 10) {
  printf("Good morning.");
} else if (time < 20) {
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
## C switch 
**Switch Statement**
- Instead of writing many `if..else` statements, one can use the switch statement.
- The switch statement selects one of many code blocks to be executed.
- Syntax
```
switch (expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```
<details>
<summary>

  **This is how it works**
</summary>

- The switch expression is evaluated once.
- The value of the expression is compared with the values of each case.
- If there is a match, the associated block of code is executed.
- The break statement breaks out of the switch block and stops the execution.
- The default statement is optional, and specifies some code to run if there is no case match.
</details>

- EXAMPLE:
```
#include <stdio.h>

int main() {
  int day = 4;
  switch (day) {
    case 1:
      printf("Monday");
      break;
    case 2:
      printf("Tuesday");
      break;
    case 3:
      printf("Wednesday");
      break;
    case 4:
      printf("Thursday");
      break;
    case 5:
      printf("Friday");
      break;
    case 6:
      printf("Saturday");
      break;
    case 7:
      printf("Sunday");
      break;
  }    
  return 0;
}
```
>OUTPUT:
><br>
>Thursday
<br>

**The break Keyword**
- When C reaches a break keyword, it breaks out of the switch block.
- This will stop the execution of more code and case testing inside the block.
<br>

```
#include <stdio.h>

int main() {
  int day = 4;
  
  switch (day) {
  case 6:
    printf("Today is Saturday");
    break;
  case 7:
    printf("Today is Sunday");
    break;
  default:
    printf("Looking forward to the Weekend");
  }
  
  return 0;
}
```
>OUTPUT
><br>
> Looking forward to the Weekend

## C While Loop
**Loops**
- Loops can execute a block of code as long as a specified condition is reached.
- Loops are handy because they save time, reduce errors, and they make code more readable.
<br>

**While Loop**
- The `while` loop loops through a block of code as long as a specified condition is `true`.
- Syntax
```
while (condition) {
  // code block to be executed
}
```
- EXAMPLE: the code in the loop will run, over and over again, as long as a variable (i) is less than 5.
```
#include <stdio.h>

int main() {
  int i = 0;
  
  while (i < 5) {
    printf("%d\n", i);
    i++;
  }
  
  return 0;
}
```
>OUTPUT
><BR>
>0
><br>
>1
><br>
>2
><br>
>3
><br>
>4

**Do-While Loop**
- The do/while loop is a variant of the while loop.
- This loop will execute the code block once, before checking if the condition is true, then it will repeat the loop as long as the condition is true.
- Syntax:
```
do {
  // code block to be executed
}
while (condition);
```
- EXAMPLE:
```
#include <stdio.h>

int main() {
  int i = 0;
  
  do {
    printf("%d\n", i);
    i++;
  }
  while (i < 5);
  
  return 0;
}
```
>OUTPUT:
><br>
>0
><br>
>1
><br>
>2
><br>
>3
><br>
>4

## C For Loop
- When we know exactly how many times we want to loop through a block of code, use the for loop instead of a while loop.
- Syntax:
```
for (expression 1; expression 2; expression 3) {
  // code block to be executed
}
```
- EXPLAINATION OF SYNTAX:
  - Expression 1 is executed (one time) before the execution of the code block.
  - Expression 2 defines the condition for executing the code block.
  - Expression 3 is executed (every time) after the code block has been executed.
- EXAMPLE:
```
#include <stdio.h>

int main() {
  int i;

  for (i = 0; i < 5; i++) {
    printf("%d\n", i);
  }
  
  return 0;
}
```
>OUTPUT
><br>
>0
><br>
>1
><br>
>2
><br>
>3
><br>
>4
- EXAMPLE EXPLAINED:
  - Expression 1 sets a variable before the loop starts (int i = 0).
  - Expression 2 defines the condition for the loop to run (i must be less than 5). If the condition is true, the loop will start over again, if it is false, the loop will end.
  - Expression 3 increases a value (i++) each time the code block in the loop has been executed.
<br>

**Nested Loops**
- It is also possible to place a loop inside another loop. This is called a nested loop.
- The "inner loop" will be executed one time for each iteration of the "outer loop".
- EXAMPLE:
```
#include <stdio.h>

int main() {
  int i, j;
  
  // Outer loop
  for (i = 1; i <= 2; ++i) {
    printf("Outer: %d\n", i);  // Executes 2 times
    
    // Inner loop
    for (j = 1; j <= 3; ++j) {
      printf(" Inner: %d\n", j);  // Executes 6 times (2 * 3)
    }
  }
  
  return 0;
}
```
>OUTPUT
><br>
>
>Outer: 1
><br>
> Inner: 1
><br>
> Inner: 2
><br>
> Inner: 3
><br>
>Outer: 2
><br>
> Inner: 1
><br>
> Inner: 2
><br>
> Inner: 3
<br>

## ARRAYS
**ARRAYS**
- Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.
- To create an array, define the data type (like `int`) and specify the name of the array followed by square brackets [].
- To insert values to it, use a comma-separated list, inside curly braces.
- Syntax
```
int myNumbers[] = {25, 50, 75, 100};
```
**Access the Elements of an Array**
- To access an array element, refer to its index number.
- Array indexes start with 0: [0] is the first element. [1] is the second element, etc.
- This statement accesses the value of the first element [0] in `myNumbers`.
- EXAMPLE:
```
#include <stdio.h>

int main() {
  int myNumbers[] = {25, 50, 75, 100};
  printf("%d", myNumbers[0]);
 
  return 0;
}
```
**Change an Array Element**
- To change the value of a specific element, refer to the index number.
- EXAMPLE:
```
myNumbers[0] = 33;
```
```
#include <stdio.h>

int main() {
  int myNumbers[] = {25, 50, 75, 100};
  myNumbers[0] = 33;

  printf("%d", myNumbers[0]);
 
  return 0;
}
```
>OUTPUT:
><br>
>33
**Set Array Size**
- Another common way to create arrays, is to specify the size of the array, and add elements later.
- EXAMPLE:
```
#include <stdio.h>

int main() {
  // Declare an array of four integers:
  int myNumbers[4];

  // Add elements to it
  myNumbers[0] = 25;
  myNumbers[1] = 50;
  myNumbers[2] = 75;
  myNumbers[3] = 100;

  printf("%d\n", myNumbers[0]);
 
  return 0;
}
```
>OUTPUT:
><br>
>25

**Get Array Size or Length**
- To get the size of an array, you can use the `sizeof` operator.
- The `sizeof` operator returns the size of a type in bytes.
- EXAMPLE:
```
#include <stdio.h>

int main() {
  int myNumbers[] = {10, 25, 50, 75, 100};
  printf("%lu", sizeof(myNumbers));
 
  return 0;
}
```
>OUTPUT:
><br>
>20
```
#include <stdio.h>

int main() {
  int myNumbers[] = {25, 50, 75, 100};
  int length = sizeof(myNumbers) / sizeof(myNumbers[0]);
  int i;

  for (i = 0; i < length; i++) {
    printf("%d\n", myNumbers[i]);
  }
  
  return 0;
}
```
>OUTPUT:
><br>
>25
><br>
>50
><br>
>75
><br>
>100

**MULTIDIMENSIONAL ARRAYS**
- A multidimensional array is basically an array of arrays.
- Arrays can have any number of dimensions.
**Two-Dimensional Arrays**
- A 2D array is also known as a matrix (a table of rows and columns).
- To create a 2D array of integers, take a look at the following example:
```
int matrix[2][3] = { {1, 4, 2}, {3, 6, 8} };
```
>EXPLAINATION:
>The first dimension represents the number of rows [2], while the second dimension represents the number of columns [3]. The values are placed in row-order, and can be visualized like this:
>||Column 0|Column 1|Column 2|
>|---|---|---|---|
>|Row 0|1|4|2|
>|Row 1|3|6|8|
**Access the Elements of a 2D Array**
- To access an element of a two-dimensional array, specify the index number of both the row and column.
- EXAMPLE:This example accesses the value of the element in the first row (0) and third column (2) of the matrix array.
```
#include <stdio.h>

int main() {
  int matrix[2][3] = { {1, 4, 2}, {3, 6, 8} };
  printf("%d", matrix[0][2]);
 
  return 0;
}
```
>OUTPUT:
><br>
>2
**Change Elements in a 2D Array**
- To change the value of an element, refer to the index number of the element in each of the dimensions:
- EXAMPLE: The following example will change the value of the element in the first row (0) and first column (0).
```
#include <stdio.h>

int main() {
  int matrix[2][3] = { {1, 4, 2}, {3, 6, 8} };
  matrix[0][0] = 9;
  printf("%d", matrix[0][0]);  // Now outputs 9 instead of 1
 
  return 0;
}
```
>OUTPUT:
><br>
>9
**Loop Through a 2D Array**
- To loop through a multi-dimensional array, you need one loop for each of the array's dimensions.
- EXAMPLE: The following example outputs all elements in the matrix array:
```
#include <stdio.h>

int main() {
  int matrix[2][3] = { {1, 4, 2}, {3, 6, 8} };

  int i, j;
  for (i = 0; i < 2; i++) {
    for (j = 0; j < 3; j++) {
      printf("%d\n", matrix[i][j]);
    }
  }
  
  return 0;
}
```
>OUTPUT:
>1
><br>
>4
><br>
>2
><br>
>3
><br>
>6
><br>
>8
<br>
**C STRINGS**
- Strings are used for storing text/characters.
- For example, "Hello World" is a string of characters.
- Unlike many other programming languages, C does not have a String type to easily create string variables. Instead, use the `char` type and create an array of characters to make a string in C.
```
char greetings[] = "Hello World!";
```
- To output the string, you can use the printf() function together with the format specifier %s to tell C that we are now working with strings.
- EXAMPLE:
```
#include <stdio.h>

int main() {
  char greetings[] = "Hello World!";
  printf("%s", greetings);
 
  return 0;
}
```
>OUTPUT: Hello World!
<br>



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


