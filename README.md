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
