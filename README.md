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