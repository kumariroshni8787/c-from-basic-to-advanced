# Day 1 - Variables, Data Types, and Input/Output in C

## Introduction

In C programming, variables are used to store data. Every variable must have a data type that tells the compiler what kind of value it will store.

---

## 1. Variables

A variable is a named memory location used to store data.

### Syntax

```c
data_type variable_name;
```

### Example

```c
int age;
float salary;
char grade;
```

### Variable Initialization

```c
int age = 20;
float salary = 25000.50;
char grade = 'A';
```

---

## 2. Data Types in C

Data types define the type of data a variable can store.

### Common Data Types

| Data Type | Description                                       | Example     |
| --------- | ------------------------------------------------- | ----------- |
| int       | Stores integer values                             | 10, -5, 100 |
| float     | Stores decimal numbers                            | 10.5, 3.14  |
| char      | Stores a single character                         | 'A', 'b'    |
| double    | Stores large decimal values with higher precision | 12.345678   |

### Example

```c
int age = 20;
float height = 5.8;
char grade = 'A';
double pi = 3.1415926535;
```

---

## 3. Input and Output

C uses standard library functions for taking input and displaying output.

### Output using `printf()`

```c
#include <stdio.h>

int main() {
    printf("Hello World");
    return 0;
}
```

### Displaying Variables

```c
#include <stdio.h>

int main() {
    int age = 20;

    printf("Age = %d", age);

    return 0;
}
```

### Common Format Specifiers

| Data Type | Format Specifier |
| --------- | ---------------- |
| int       | %d               |
| float     | %f               |
| char      | %c               |
| double    | %lf              |

---

## 4. Input using `scanf()`

### Example

```c
#include <stdio.h>

int main() {
    int age;

    printf("Enter your age: ");
    scanf("%d", &age);

    printf("Your age is %d", age);

    return 0;
}
```

### Why `&` is Used?

The `&` operator gives the memory address of a variable so that `scanf()` can store the entered value in that variable.

Example:

```c
scanf("%d", &age);
```

---

## Complete Program Example

```c
#include <stdio.h>

int main() {
    int age;
    float height;
    char grade;

    printf("Enter age: ");
    scanf("%d", &age);

    printf("Enter height: ");
    scanf("%f", &height);

    printf("Enter grade: ");
    scanf(" %c", &grade);

    printf("\n--- Student Details ---\n");
    printf("Age: %d\n", age);
    printf("Height: %.2f\n", height);
    printf("Grade: %c\n", grade);

    return 0;
}
```

---

## Key Points

* Variables store data in memory.
* Every variable must have a data type.
* `int`, `float`, `char`, and `double` are commonly used data types.
* `printf()` is used for output.
* `scanf()` is used for input.
* Format specifiers are used to match data types.
* `&` is required in `scanf()` for most variables.

---

## Practice Questions

1. Create a program to store and display your name, age, and percentage.
2. Take two integer inputs from the user and display them.
3. Create variables of different data types and print their values.
4. Write a program that takes a character input and displays it.

---
📌 Day 1 Summary
Learned what variables are and why they are used.
Studied basic C data types (int, float, char, double).
Learned how to display output using printf().
Learned how to take user input using scanf().
Understood format specifiers and the use of the & operator.

# Day 2 - Instructions and Operators in C

## Introduction

A C program is made up of instructions that tell the computer what to do. Operators are symbols used to perform operations on data and variables.

---

## 1. Instructions in C

Instructions are statements executed by the computer.

### Types of Instructions

### A) Type Declaration Instruction

Used to declare variables before using them.

```c
int age;
float salary;
char grade;
```

### B) Arithmetic Instruction

Used to perform mathematical calculations.

```c
int sum = 10 + 20;
int difference = 20 - 10;
int product = 10 * 5;
int quotient = 20 / 4;
```

### C) Control Instruction

Used to control the flow of a program.

Examples:

```c
if (age >= 18)
{
    printf("Adult");
}
```

```c
for(int i = 1; i <= 5; i++)
{
    printf("%d\n", i);
}
```

---

## 2. Operators in C

Operators are special symbols used to perform operations on variables and values.

---

## A) Arithmetic Operators

| Operator | Meaning             | Example |
| -------- | ------------------- | ------- |
| +        | Addition            | a + b   |
| -        | Subtraction         | a - b   |
| *        | Multiplication      | a * b   |
| /        | Division            | a / b   |
| %        | Modulus (Remainder) | a % b   |

### Example

```c
#include <stdio.h>

int main()
{
    int a = 10, b = 3;

    printf("Addition = %d\n", a + b);
    printf("Subtraction = %d\n", a - b);
    printf("Multiplication = %d\n", a * b);
    printf("Division = %d\n", a / b);
    printf("Remainder = %d\n", a % b);

    return 0;
}
```

---

## B) Relational Operators

Used to compare values.

| Operator | Meaning                  |
| -------- | ------------------------ |
| ==       | Equal to                 |
| !=       | Not equal to             |
| >        | Greater than             |
| <        | Less than                |
| >=       | Greater than or equal to |
| <=       | Less than or equal to    |

### Example

```c
int a = 10;
int b = 20;

printf("%d", a < b);
```

Output:

```text
1
```

(1 = True, 0 = False)

---

## C) Logical Operators

Used to combine conditions.

| Operator | Meaning |   |    |
| -------- | ------- | - | -- |
| &&       | AND     |   |    |
|          |         |   | OR |
| !        | NOT     |   |    |

### Example

```c
int age = 20;

if(age > 18 && age < 60)
{
    printf("Eligible");
}
```

---

## D) Assignment Operators

Used to assign values.

| Operator | Example |
| -------- | ------- |
| =        | a = 10  |
| +=       | a += 5  |
| -=       | a -= 5  |
| *=       | a *= 5  |
| /=       | a /= 5  |

### Example

```c
int a = 10;

a += 5;

printf("%d", a);
```

Output:

```text
15
```

---

## E) Increment and Decrement Operators

### Increment (++)

Increases value by 1.

```c
int a = 5;
a++;
```

Value becomes:

```text
6
```

### Decrement (--)

Decreases value by 1.

```c
int a = 5;
a--;
```

Value becomes:

```text
4
```

---

## Pre and Post Increment

### Pre Increment

```c
int a = 5;
int b = ++a;
```

Result:

```text
a = 6
b = 6
```

### Post Increment

```c
int a = 5;
int b = a++;
```

Result:

```text
a = 6
b = 5
```

---

## Operator Precedence (Basic)

Priority order:

```text
()
*, /, %
+, -
<, >, <=, >=
==, !=
&&
||
=
```

Example:

```c
int result = 10 + 5 * 2;
```

Output:

```text
20
```

Because multiplication is performed first.

---

## Key Points

* Instructions are statements executed by the program.
* Operators perform calculations and comparisons.
* Arithmetic operators are used for mathematical operations.
* Relational operators return true (1) or false (0).
* Logical operators combine conditions.
* Assignment operators simplify value updates.
* Increment and decrement operators change values by 1.
* Operator precedence determines execution order.

---

## Practice Questions

1. Take two numbers and perform all arithmetic operations.
2. Check whether one number is greater than another.
3. Use logical operators to check age eligibility.
4. Write a program using += and -= operators.
5. Demonstrate pre-increment and post-increment with examples.

---
📌 Day 2 Summary
Learned different types of instructions in C.
Studied arithmetic, relational, logical, assignment, increment, and decrement operators.
Understood the difference between pre-increment and post-increment.
Learned basic operator precedence.


# Day 3 - Conditional Statements in C

## Introduction

Conditional statements help a program make decisions based on conditions.

They allow the program to execute different blocks of code depending on whether a condition is true or false.

---

## 1. if Statement

The `if` statement executes a block of code only when the condition is true.

### Syntax

```c
if(condition)
{
    // code
}
```

### Example

```c
#include <stdio.h>

int main()
{
    int age = 20;

    if(age >= 18)
    {
        printf("You are eligible to vote.");
    }

    return 0;
}
```

---

## 2. if-else Statement

Used when there are two possible outcomes.

### Syntax

```c
if(condition)
{
    // code if true
}
else
{
    // code if false
}
```

### Example

```c
#include <stdio.h>

int main()
{
    int number;

    printf("Enter a number: ");
    scanf("%d", &number);

    if(number % 2 == 0)
    {
        printf("Even Number");
    }
    else
    {
        printf("Odd Number");
    }

    return 0;
}
```

---

## 3. else-if Ladder

Used when multiple conditions need to be checked.

### Syntax

```c
if(condition1)
{
    // code
}
else if(condition2)
{
    // code
}
else
{
    // code
}
```

### Example

```c
#include <stdio.h>

int main()
{
    int marks;

    printf("Enter marks: ");
    scanf("%d", &marks);

    if(marks >= 90)
    {
        printf("Grade A");
    }
    else if(marks >= 75)
    {
        printf("Grade B");
    }
    else if(marks >= 50)
    {
        printf("Grade C");
    }
    else
    {
        printf("Fail");
    }

    return 0;
}
```

---

## 4. Nested if

An `if` statement inside another `if` statement.

### Example

```c
#include <stdio.h>

int main()
{
    int age = 20;
    int citizen = 1;

    if(age >= 18)
    {
        if(citizen == 1)
        {
            printf("Eligible to vote");
        }
    }

    return 0;
}
```

---

## 5. switch Statement

Used when there are multiple fixed choices.

### Syntax

```c
switch(expression)
{
    case value1:
        // code
        break;

    case value2:
        // code
        break;

    default:
        // code
}
```

### Example

```c
#include <stdio.h>

int main()
{
    int day;

    printf("Enter day number (1-7): ");
    scanf("%d", &day);

    switch(day)
    {
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

        default:
            printf("Invalid Day");
    }

    return 0;
}
```

---

## Difference Between if-else and switch

| if-else                                  | switch                                   |
| ---------------------------------------- | ---------------------------------------- |
| Works with conditions                    | Works with fixed values                  |
| Can use relational and logical operators | Cannot use relational operators in cases |
| Better for complex conditions            | Better for menu-driven programs          |

---

## Key Points

* `if` executes code when a condition is true.
* `if-else` handles two outcomes.
* `else-if` ladder handles multiple conditions.
* Nested `if` means an `if` inside another `if`.
* `switch` is useful when selecting from multiple fixed options.
* `break` prevents execution from continuing to the next case.

---

## Practice Questions

1. Check whether a number is positive or negative.
2. Check whether a number is even or odd.
3. Find the largest of two numbers using `if-else`.
4. Display grades using an `else-if` ladder.
5. Create a simple calculator using `switch`.

---
📌 Day 3 Summary
Learned decision-making in C using conditional statements.
Studied if, if-else, else-if, and nested if.
Learned how to use the switch statement.
Understood the difference between if-else and switch.

# Day 4 - Loop Control Statements in C

## Introduction

Loop control statements are used to execute a block of code repeatedly until a condition becomes false.

Loops help reduce code repetition and make programs more efficient.

---

## 1. while Loop

The `while` loop checks the condition first and then executes the code.

### Syntax

```c
while(condition)
{
    // code
}
```

### Example

```c
#include <stdio.h>

int main()
{
    int i = 1;

    while(i <= 5)
    {
        printf("%d\n", i);
        i++;
    }

    return 0;
}
```

### Output

```text
1
2
3
4
5
```

---

## 2. do-while Loop

The `do-while` loop executes the code once before checking the condition.

### Syntax

```c
do
{
    // code
}
while(condition);
```

### Example

```c
#include <stdio.h>

int main()
{
    int i = 1;

    do
    {
        printf("%d\n", i);
        i++;
    }
    while(i <= 5);

    return 0;
}
```

---

## 3. for Loop

The `for` loop is commonly used when the number of iterations is known.

### Syntax

```c
for(initialization; condition; update)
{
    // code
}
```

### Example

```c
#include <stdio.h>

int main()
{
    int i;

    for(i = 1; i <= 5; i++)
    {
        printf("%d\n", i);
    }

    return 0;
}
```

---

## Comparison of Loops

| Loop     | Condition Check  |
| -------- | ---------------- |
| while    | Before execution |
| do-while | After execution  |
| for      | Before execution |

---

## 4. break Statement

The `break` statement immediately terminates the loop.

### Example

```c
#include <stdio.h>

int main()
{
    int i;

    for(i = 1; i <= 10; i++)
    {
        if(i == 5)
        {
            break;
        }

        printf("%d\n", i);
    }

    return 0;
}
```

### Output

```text
1
2
3
4
```

---

## 5. continue Statement

The `continue` statement skips the current iteration and moves to the next iteration.

### Example

```c
#include <stdio.h>

int main()
{
    int i;

    for(i = 1; i <= 5; i++)
    {
        if(i == 3)
        {
            continue;
        }

        printf("%d\n", i);
    }

    return 0;
}
```

### Output

```text
1
2
4
5
```

---

## 6. Infinite Loop

A loop that never ends is called an infinite loop.

### Example

```c
while(1)
{
    printf("Hello");
}
```

Use carefully because the loop will run forever unless stopped manually.

---

## Key Points

* Loops are used to repeat a block of code.
* `while` checks the condition before execution.
* `do-while` executes at least once.
* `for` loop is best when the number of repetitions is known.
* `break` exits the loop immediately.
* `continue` skips the current iteration.
* Infinite loops run forever.

---

## Practice Questions

1. Print numbers from 1 to 10 using a `while` loop.
2. Print numbers from 10 to 1 using a `for` loop.
3. Print the multiplication table of a number.
4. Find the sum of the first 10 natural numbers.
5. Print even numbers from 1 to 100.
6. Demonstrate `break` and `continue` using examples.

---
📌 Day 4 Summary
Learned about loop control statements in C.
Studied while, do-while, and for loops.
Understood the difference between loop types.
Learned how break and continue affect loop execution.
Practiced repeating tasks efficiently using loops.




# Day 5 - Functions and Recursion in C

## Introduction

Functions are blocks of code designed to perform a specific task. They help make programs modular, reusable, and easier to understand.

Recursion is a technique where a function calls itself to solve a problem.

---

## 1. What is a Function?

A function is a collection of statements that performs a specific task.

### Benefits of Functions

* Code reusability
* Better organization
* Easier debugging
* Reduces code duplication

---

## 2. Function Syntax

```c
return_type function_name(parameters)
{
    // code
    return value;
}
```

### Example

```c
#include <stdio.h>

void greet()
{
    printf("Welcome to C Programming!");
}

int main()
{
    greet();

    return 0;
}
```

---

## 3. Function Declaration, Definition, and Call

### Declaration (Prototype)

```c
int add(int, int);
```

### Definition

```c
int add(int a, int b)
{
    return a + b;
}
```

### Function Call

```c
int result = add(10, 20);
```

---

## 4. Types of Functions

### A) No Arguments, No Return Value

```c
void display()
{
    printf("Hello");
}
```

### B) Arguments, No Return Value

```c
void display(int age)
{
    printf("%d", age);
}
```

### C) No Arguments, Return Value

```c
int getNumber()
{
    return 10;
}
```

### D) Arguments and Return Value

```c
int add(int a, int b)
{
    return a + b;
}
```

---

## 5. Example: Sum of Two Numbers

```c
#include <stdio.h>

int add(int a, int b)
{
    return a + b;
}

int main()
{
    int num1, num2;

    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

    printf("Sum = %d", add(num1, num2));

    return 0;
}
```

---

## 6. Recursion

Recursion is a process in which a function calls itself.

### Basic Structure

```c
void function()
{
    function();
}
```

A recursive function must have a **base condition**, otherwise it will run forever.

---

## 7. Factorial Using Recursion

### Formula

```text
5! = 5 × 4 × 3 × 2 × 1
```

### Recursive Program

```c
#include <stdio.h>

int factorial(int n)
{
    if(n == 0 || n == 1)
    {
        return 1;
    }

    return n * factorial(n - 1);
}

int main()
{
    int num;

    printf("Enter a number: ");
    scanf("%d", &num);

    printf("Factorial = %d", factorial(num));

    return 0;
}
```

### Example

```text
Input: 5
Output: 120
```

---

## 8. Recursion vs Loop

| Recursion                | Loop                |
| ------------------------ | ------------------- |
| Function calls itself    | Repeats using loops |
| Easier for some problems | Usually faster      |
| Uses more memory         | Uses less memory    |

---

## Key Points

* Functions divide a program into smaller parts.
* Functions can take arguments and return values.
* Function declaration informs the compiler about a function.
* Recursion means a function calls itself.
* Every recursive function must have a base condition.
* Factorial is a common example of recursion.

---

## Practice Questions

1. Create a function to find the square of a number.
2. Create a function to find the largest of two numbers.
3. Write a function to calculate the area of a circle.
4. Find the factorial of a number using recursion.
5. Print numbers from 1 to N using recursion.

---
📌 Day 5 Summary
Learned about functions and their advantages.
Understood function declaration, definition, and function calls.
Studied different types of functions.
Learned the concept of recursion.
Implemented factorial using recursion.