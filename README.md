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