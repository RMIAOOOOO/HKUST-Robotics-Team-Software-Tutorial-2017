# C Programming

Author: Christopher Wong<br>
Contact: pkcwongab@ust.hk<br>
[Find me on GitHub](https://github.com/pkcwong)

---

## File System

C language code files involves two file types.
- ```.h``` contains structure and function declarations
- ```.c``` contains function implementations

## Basic Structure

A project written in C must implement the program entry function ```int main(void)```, which is usually found in ```main.c```.

```C

  /*
   * file: main.c
   */

  int main(void)  // program entry point
  {
    // code here
  }

```

## Variables

Variables are "boxes" that hold data.

Some primitive data types in C. These data types are native to C.
- ```char```
- ```int```
- ```float```
- ```double```

Also some common non-primitive data types we may encounter. Appropriate libraries must be included before usage.
- ```bool``` (available in ```<stdbool.h>```)
- ```size_t``` (available in ```<stdlib.h>```)

To declare a variable, the syntax is the data type identifier followed by its name.

```C

  int main()
  {
    char haha;
    int hoho;
    double hehe;
  }

```

To assign a value to a variable, use the ```=``` operator.

```C

  int main()
  {
    char haha;
    int hoho;
    double hehe;
    haha = 'a';
    hoho = 64;
    hehe = 3.1415926535897932;
  }

```

## Standard Input / Output

Standard input / output functions may be found in library ```<stdio.h>```.

### Console Output

Function ```void printf(const char*, ...)``` prints to console.

```C

  #include <stdio.h>

  int main()
  {
    printf("Hello World!"); // prints "Hello World!" on console
  }

```

To print the value of a variable, specify the data type token and provide the variable as additional argument.

```C

  int main()
  {
    int hoho = 123;
    double hehe = 0.618;
    printf("%d %f", hoho, hehe);  // prints "123 0.618"
  }

```

Data type tokens can be referred from the table below. Common usage in *italic*.

Token | Group | Applicable Data Types
--- | --- | ---
%d | Decimals | char, *int*
%f | Floating Points | *float*, *double*
%x | Hexadecimals | char, *int*
%c | Characters | *char*, int

### Console Input

Function ```void scanf(const char*, ...)``` stores an input from console to a variable. Specify the data type token and provide the address to the variable. Similar to ```printf```, but an ampersand(&) is required before the variable name.

> For further reading on address and memory location, see my other tutorial notes ```data-structure.md``` on C pointers.

```C

  int main()
  {
    int hoho;
    scanf("%d", &hoho);
  }

```

## Operators

An operator assigns or modifies a variable or value.
- ```=``` assignment
- ```+``` addition
- ```-``` subtraction
- ```*``` multiplication
- ```/``` division
- ```%``` modulo
- ```()``` parentheses

## Comparators

A comparator compares the value of two expressions, most of which are self explanatory.
- ```==``` equal to
- ```!=``` not equal to
- ```>``` greater than
- ```>=``` greater than or equal to
- ```<``` less than
- ```<=``` less than or equal to

## Statements

A statement is an expression which can be evaluated to either 1 or 0, or in other words true or false. The evaluated value of a statement can be stored by a ```bool```.

```C

  int main()
  {
    bool statement = (2 > 1); // true
  }

```

## Conditionals

Conditionals are flow controls which guide the execution of a program based on statement evaluations.

### If-Else

Self explanatory.

```C

  int main()
  {
    int a;

    scanf("%d", &a);
    if (a > 50)
    {
      printf("greater than 50.\n");
    }
    else
    {
      printf("not greater than 50.\n")
    }
  }

```

### Switch-Case

Switch-Case allows a variable or expression to be tested for equality against a list of values.

```C

  int main()
  {
    int a;
    scanf("%d", &a);
    switch (a % 2)
    {
      case 0:
        printf("even");
        break;
      default:
        printf("odd");
    }
  }

```

### Do-While

While loop blocks execute as long as the condition is met.

```C

  int main()
  {
    int i = 0;
    while (i != 10)
    {
      printf("Hello\n");  // prints 10 times
      i++;
    }
  }

```

Do-While loop blocks execute at least once, terminating when condition is no longer met.

```C

  int main()
  {
    int i = 0;
    do
    {
      printf("Hello\n");  // prints 10 times
      i++;
    }
    while(i != 10);
  }

```

### For-loops

Similar to while loops, but with its own counter.

```C

  int main()
  {
    for (int i = 0; i != 10; i++)
    {
      printf("Hello\n");  // prints 10 times
    }
  }

```

### Break-Continue

## Functions
