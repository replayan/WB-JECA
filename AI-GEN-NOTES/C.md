# C Programming

## Variables and Data Types
- **Variables**: Named storage locations in memory to hold values.
  - **Declaration**: `data_type variable_name;`
  - **Example**: `int age;`
- **Data Types**:
  - **Basic Types**: `int`, `char`, `float`, `double`
  - **Derived Types**: Arrays, Pointers, Structures, Unions
  - **Void Type**: `void`
  - **Example**:
    ```c
    int age = 25;
    char grade = 'A';
    float salary = 55000.50;
    ```

## IO Operations
- **Input/Output Functions**:
  - **Standard Input**: `scanf()`
  - **Standard Output**: `printf()`
  - **Example**:
    ```c
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    printf("You entered: %d", num);
    ```

## Operators and Expressions
- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`
- **Relational Operators**: `==`, `!=`, `>`, `<`, `>=`, `<=`
- **Logical Operators**: `&&`, `||`, `!`
- **Bitwise Operators**: `&`, `|`, `^`, `~`, `<<`, `>>`
- **Assignment Operators**: `=`, `+=`, `-=`, `*=`, `/=`, `%=`
- **Increment/Decrement Operators**: `++`, `--`
- **Example**:
  ```c
  int a = 10, b = 20;
  int sum = a + b;
  int isEqual = (a == b);
  ```

## Control Flow Statements
- **Conditional Statements**:
  - **if**:
    ```c
    if (condition) {
        // statements
    }
    ```
  - **if-else**:
    ```c
    if (condition) {
        // statements
    } else {
        // statements
    }
    ```
  - **else-if Ladder**:
    ```c
    if (condition1) {
        // statements
    } else if (condition2) {
        // statements
    } else {
        // statements
    }
    ```
  - **switch-case**:
    ```c
    switch (expression) {
        case constant1:
            // statements
            break;
        case constant2:
            // statements
            break;
        default:
            // statements
    }
    ```
- **Looping Statements**:
  - **for Loop**:
    ```c
    for (initialization; condition; increment) {
        // statements
    }
    ```
  - **while Loop**:
    ```c
    while (condition) {
        // statements
    }
    ```
  - **do-while Loop**:
    ```c
    do {
        // statements
    } while (condition);
    ```

## Functions
- **Definition**: Block of code performing a specific task, reusable.
- **Syntax**:
  ```c
  return_type function_name(parameters) {
      // function body
      return value;
  }
  ```
- **Example**:
  ```c
  int add(int a, int b) {
      return a + b;
  }
  int main() {
      int sum = add(5, 10);
      printf("Sum: %d", sum);
      return 0;
  }
  ```

## Array
- **Definition**: Collection of elements of the same type.
- **Syntax**:
  ```c
  data_type array_name[array_size];
  ```
- **Example**:
  ```c
  int arr[5] = {1, 2, 3, 4, 5};
  ```

## Pointers
- **Definition**: Variables that store memory addresses.
- **Syntax**:
  ```c
  data_type *pointer_name;
  ```
- **Example**:
  ```c
  int value = 10;
  int *ptr = &value;
  printf("Value: %d, Address: %p", *ptr, ptr);
  ```

## String Handling
- **String Definition**: Array of characters terminated by a null character `\0`.
- **Functions**:
  - **strlen()**: Returns the length of the string.
  - **strcpy()**: Copies one string to another.
  - **strcat()**: Concatenates two strings.
  - **strcmp()**: Compares two strings.
- **Example**:
  ```c
  char str1[20] = "Hello";
  char str2[20];
  strcpy(str2, str1);
  strcat(str2, " World");
  int len = strlen(str2);
  int cmp = strcmp(str1, "Hello");
  ```

# Structures and Unions in C

## Structures

### Definition
- **Structures** are user-defined data types that group different data types together. They are used to represent a record.

### Declaration and Definition
- **Syntax**:
  ```c
  struct StructureName {
      data_type member1;
      data_type member2;
      // More members
  };
  ```
- **Example**:
  ```c
  struct Person {
      char name[50];
      int age;
      float salary;
  };
  ```

### Accessing Members
- **Creating an Instance**:
  ```c
  struct Person person1;
  ```
- **Accessing Members**:
  - Using the dot operator `.`:
    ```c
    person1.age = 30;
    strcpy(person1.name, "John");
    person1.salary = 50000.50;
    ```

### Nested Structures
- **Definition**: Structures within structures.
- **Example**:
  ```c
  struct Address {
      char street[50];
      char city[50];
      int zip;
  };

  struct Employee {
      char name[50];
      struct Address addr;
      float salary;
  };

  struct Employee emp1;
  emp1.addr.zip = 12345;
  ```

### Array of Structures
- **Definition**: Arrays where each element is a structure.
- **Example**:
  ```c
  struct Person people[5];

  people[0].age = 25;
  strcpy(people[0].name, "Alice");
  people[0].salary = 30000;
  ```

### Structure Pointers
- **Definition**: Pointers that point to structures.
- **Example**:
  ```c
  struct Person *ptr;
  ptr = &person1;

  ptr->age = 45;  // Using arrow operator to access members via pointer
  ```

### Memory Allocation for Structures
- **Static Allocation**:
  ```c
  struct Person person2;
  ```
- **Dynamic Allocation**:
  ```c
  struct Person *ptr;
  ptr = (struct Person*)malloc(sizeof(struct Person));
  ```

### Typedef with Structures
- **Definition**: Simplifying structure declarations using `typedef`.
- **Example**:
  ```c
  typedef struct Person {
      char name[50];
      int age;
      float salary;
  } Person;

  Person p1;
  ```

## Unions

### Definition
- **Unions** are user-defined data types where all members share the same memory location. Only one member can contain a value at any given time.

### Declaration and Definition
- **Syntax**:
  ```c
  union UnionName {
      data_type member1;
      data_type member2;
      // More members
  };
  ```
- **Example**:
  ```c
  union Data {
      int i;
      float f;
      char str[20];
  };
  ```

### Accessing Members
- **Creating an Instance**:
  ```c
  union Data data;
  ```
- **Accessing Members**:
  - Using the dot operator `.`:
    ```c
    data.i = 10;
    printf("data.i: %d\n", data.i);

    data.f = 220.5;
    printf("data.f: %f\n", data.f);

    strcpy(data.str, "C Programming");
    printf("data.str: %s\n", data.str);
    ```

### Differences Between Structures and Unions
| Feature        | Structure | Union |
|----------------|-----------|-------|
| Memory         | Allocates memory for all members. | Allocates memory equal to the largest member. |
| Member Access  | All members can be accessed independently. | Only one member can be accessed at a time. |
| Use Case       | Used when you need to store multiple related data. | Used when you need to store one of several types of data. |

### Example with Structures and Unions

#### Structure Example
```c
#include <stdio.h>
#include <string.h>

struct Student {
    char name[50];
    int age;
    float gpa;
};

int main() {
    struct Student student1;

    strcpy(student1.name, "Alice");
    student1.age = 20;
    student1.gpa = 3.9;

    printf("Name: %s\n", student1.name);
    printf("Age: %d\n", student1.age);
    printf("GPA: %.2f\n", student1.gpa);

    return 0;
}
```

#### Union Example
```c
#include <stdio.h>
#include <string.h>

union Data {
    int i;
    float f;
    char str[20];
};

int main() {
    union Data data;

    data.i = 10;
    printf("data.i: %d\n", data.i);

    data.f = 220.5;
    printf("data.f: %f\n", data.f);

    strcpy(data.str, "C Programming");
    printf("data.str: %s\n", data.str);

    return 0;
}
```

### Real-World Application of Unions
- **Example**: Storing data packets where the packet can be of different types.
  ```c
  union Packet {
      int integerPacket;
      float floatPacket;
      char strPacket[50];
  };

  void processPacket(union Packet pkt, int type) {
      switch (type) {
          case 1:
              printf("Integer Packet: %d\n", pkt.integerPacket);
              break;
          case 2:
              printf("Float Packet: %f\n", pkt.floatPacket);
              break;
          case 3:
              printf("String Packet: %s\n", pkt.strPacket);
              break;
      }
  }
  ```

## File Handling
- **Functions**:
  - **fopen()**: Opens a file.
  - **fclose()**: Closes a file.
  - **fread()**: Reads data from a file.
  - **fwrite()**: Writes data to a file.
  - **fprintf()**: Writes formatted output to a file.
  - **fscanf()**: Reads formatted input from a file.
- **Modes**:
  - `"r"`: Read
  - `"w"`: Write
  - `"a"`: Append
  - `"r+"`: Read/Write
  - `"w+"`: Write/Read
  - `"a+"`: Append/Read
- **Example**:
  ```c
  FILE *fp;
  fp = fopen("file.txt", "w");
  if (fp != NULL) {
      fprintf(fp, "Hello, World!");
      fclose(fp);
  }
  ```

## Pre-Processor Directives
- **Definition**: Commands processed by the preprocessor before compilation.
- **Common Directives**:
  - `#define`: Defines a macro.
    ```c
    #define PI 3.14
    ```
  - `#include`: Includes a file.
    ```c
    #include <stdio.h>
    #include "myfile.h"
    ```
  - `#if`, `#else`, `#elif`, `#endif`: Conditional compilation.
    ```c
    #if defined(MACRO)
        // statements
    #else
        // statements
    #endif
    ```

## Command Line Arguments
- **Definition**: Arguments passed to `main` from the command line.
- **Syntax**:
  ```c
  int main(int argc, char *argv[]) {
      // argc: argument count
      // argv: argument vector (array of strings)
  }
  ```
- **Example**:
  ```c
  int main(int argc, char *argv[]) {
      if (argc > 1) {
          printf("Argument: %s\n", argv[1]);
      }
      return 0;
  }
  ```
