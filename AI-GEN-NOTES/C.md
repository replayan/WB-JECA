# C Language

---

### Key Points
- Variables in C store data and must have a declared data type like int or char, with rules for naming.
- IO operations use `printf` for output and `scanf` for input, handling formatted data.
- Operators include arithmetic (+, -, *), relational (==, <), and logical (&&, ||), forming expressions.
- Control flow statements like if-else, loops (for, while), and switch manage program execution order.
- Functions are reusable code blocks, with parameters and return types, supporting recursion.
- Arrays store multiple values of the same type, accessed by index, with multi-dimensional support.
- Pointers hold memory addresses, enabling dynamic memory and efficient parameter passing.
- Strings are character arrays, handled with functions like `strlen` and `strcpy` from `<string.h>`.
- Structures group different data types, while unions share memory for members, optimizing space.
- File handling involves reading/writing with functions like `fopen` and `fclose`, using modes like "r" or "w".
- Pre-processor directives like `#include` and `#define` prepare code before compilation.
- Command line arguments allow passing inputs at program start, accessed via `main`'s `argc` and `argv`.

### Variables and Data Types
Variables are named memory locations storing data, requiring a declared type like `int`, `char`, `float`, or `double`. C is statically typed, meaning types are fixed at declaration. Naming rules include starting with a letter or underscore, using only letters, digits, and underscores, no spaces, and avoiding keywords.

**Primitive Data Types:**
- `int`: Whole numbers, typically 4 bytes, range -2,147,483,648 to 2,147,483,647, format `%d`.
- `char`: Single character, 1 byte, range -128 to 127 or 0 to 255, format `%c`.
- `float`: Single-precision floating-point, 4 bytes, range ~1.2E-38 to 3.4E+38, format `%f`.
- `double`: Double-precision, 8 bytes, range ~1.7E-308 to 1.7E+308, format `%lf`.
- `void`: Indicates no value, used for pointers or functions without return.

Modifiers like `long`, `short`, `signed`, `unsigned` adjust size or range. Sizes vary by system; use `sizeof()` to check, e.g., on 64-bit GCC:
| Data Type           | Size (bytes) | Range                              | Format Specifier |
|--------------------|--------------|------------------------------------|------------------|
| short int          | 2            | -32,768 to 32,767                 | %hd              |
| unsigned short int | 2            | 0 to 65,535                       | %hu              |
| int                | 4            | -2,147,483,648 to 2,147,483,647   | %d               |
| long int           | 4            | -2,147,483,648 to 2,147,483,647   | %ld              |
| float              | 4            | 1.2E-38 to 3.4E+38                | %f               |
| double             | 8            | 1.7E-308 to 1.7E+308              | %lf              |

Constants, declared with `const`, have fixed values, e.g., `const int MAX = 100`.

### IO Operations
IO operations handle data input/output, primarily via console using `printf` for output and `scanf` for input. `printf` prints formatted output, e.g., `printf("Age: %d\n", age);` outputs "Age: 25" with newline. `scanf` reads input, e.g., `scanf("%d", &age);` stores user input into `age`. Format specifiers match data types: `%d` for int, `%f` for float, `%c` for char, `%s` for strings. Use `&` with `scanf` for variable addresses. Other functions include `getchar()`, `putchar()`, `gets()`, `puts()`, but `printf` and `scanf` are standard for formatted IO.

### Operators and Expressions
Operators perform operations on operands, classified as:
- **Arithmetic:** +, -, *, /, %, ++, --, e.g., `a + b`.
- **Relational:** ==, !=, <, >, <=, >=, return 1 (true) or 0 (false), e.g., `a == b`.
- **Logical:** && (AND), || (OR), ! (NOT), combine conditions, e.g., `a && b`.
- **Bitwise:** &, |, ^, ~, <<, >>, operate on bits, e.g., `a & b`.
- **Assignment:** =, +=, -=, *=, /=, %=, etc., e.g., `a += 5`.
- **Other:** sizeof, comma (,), conditional (?:), dot (.), arrow (->), cast, addressof (&), dereference (*).

Expressions combine operators and operands, e.g., `a + b * c`. Precedence and associativity determine evaluation order; use parentheses for clarity, e.g., `(a + b) * c`.

### Control Flow Statements
Control flow statements manage execution order:
- **Conditional:** `if`, `if-else`, `if-else-if`, `switch-case`, ternary operator (?:), e.g., `if (a > 0) printf("Positive");`.
- **Loops:** `for` (e.g., `for(int i=0; i<5; i++)`), `while` (e.g., `while(count<5)`), `do-while` (executes at least once), nested loops for multi-dimensional iteration.
- **Jump:** `break` exits loops/switches, `continue` skips iterations, `return` exits functions, `goto` jumps to labels (discouraged for readability).

These enable decision-making and repetition, crucial for program logic.

### Functions
Functions are reusable code blocks performing specific tasks. Declare with return type and parameters, e.g., `int add(int a, int b);`. Define with body, e.g., `int add(int a, int b) { return a + b; }`. Call with arguments, e.g., `result = add(5, 6);`. Types include library (e.g., `printf`) and user-defined. Parameters pass by value or reference (via pointers). Functions can be recursive, e.g., factorial calculation. Return type can be `void` for no return.

### Array
Arrays store multiple same-type elements contiguously. Declare as `int arr[5];`, initialize `int arr[] = {1, 2, 3};`. Access via index, e.g., `arr[0]`. Multi-dimensional, e.g., `int matrix[2][3]` for 2D. Passed to functions as pointers, requiring careful bounds management to avoid overflow.

### Pointers
Pointers store memory addresses, declared as `int *ptr;`. Initialize with `ptr = &var;`, dereference with `*ptr` to access value. Used for dynamic memory (e.g., `malloc`), passing by reference, array access. Support arithmetic, e.g., `ptr++` moves to next element. Concepts include null pointers, dangling pointers, pointer-to-pointer for complex data.

### String Handling
Strings are char arrays ending with '\0'. Declare as `char str[10];` or `char *str = "Hello";`. Handle with `<string.h>` functions: `strlen` for length, `strcpy` for copy, `strcat` for concatenation, `strcmp` for comparison. Ensure null terminator for proper handling.

### Structures and Unions
- **Structures:** Group different types, e.g., `struct Student { char name[50]; int age; };`. Access with dot operator, e.g., `student.age`. Useful for complex data.
- **Unions:** Share memory, e.g., `union Data { int i; float f; };`. Only one member active at a time, saving space, e.g., for type-agnostic storage.

### Files Handling
File handling reads/writes external files. Use `fopen` to open (modes: "r" read, "w" write, "a" append), `fclose` to close. Read/write with `fread`, `fwrite`, or formatted `fprintf`, `fscanf`. Check file operations for success, e.g., `if (fp == NULL) printf("Error");`.

### Pre-Processor Directives
Pre-process before compilation, starting with `#`. Include headers with `#include <stdio.h>`, define macros with `#define PI 3.14`. Conditional compilation with `#if`, `#ifdef`, `#ifndef`, `#else`, `#endif` for code portability.

### Command Line Arguments
Pass inputs at execution, accessed via `main(int argc, char *argv[])`. `argc` is argument count, `argv` is string array. `argv[0]` is program name, e.g., `./program 10 20` has `argc=3`, `argv[0]="./program"`, `argv[1]="10"`. Useful for flexible programs.

---

### Detailed Notes for WB-JECA Exam

#### Variables and Data Types
Variables are named memory locations storing data, essential for programming. In C, each variable must have a declared data type, as C is statically typed, meaning types are fixed at declaration and cannot change, due to varying memory needs and type-specific operations. Declaration syntax is `data_type variable_name;`, e.g., `int age;`, with initialization possible, e.g., `int age = 25;`.

**Naming Rules:**
- Must start with a letter or underscore.
- Can include letters, digits, underscores, no spaces.
- Case-sensitive, e.g., `Age` and `age` differ.
- Cannot be keywords like `int`, `while`.

**Data Types Classification:**
- **Primitive:** Basic types for simple values.
  - `int`: Stores integers, typically 4 bytes, range -2,147,483,648 to 2,147,483,647, format `%d`. Variants include `short int` (2 bytes, -32,768 to 32,767), `long int` (4 or 8 bytes, larger range), `unsigned int` (0 to positive, no negatives).
  - `char`: Single character, 1 byte, range -128 to 127 (signed) or 0 to 255 (unsigned), format `%c`.
  - `float`: Single-precision floating-point, 4 bytes, range ~1.2E-38 to 3.4E+38, format `%f`.
  - `double`: Double-precision, 8 bytes, range ~1.7E-308 to 1.7E+308, format `%lf`.
  - `void`: No value, used for pointers, functions without return.

- **Derived:** Array, pointers, function (covered separately).
- **User Defined:** Structure, union, enum (covered separately).

**Modifiers:** `long`, `short`, `signed`, `unsigned` adjust size/range, e.g., `unsigned char` for 0-255 range.

**Size and Range:** Vary by system; use `sizeof()` operator, e.g., `sizeof(int)` returns 4 on 64-bit GCC. Example table for 64-bit GCC:
| Data Type           | Size (bytes) | Range                              | Format Specifier |
|--------------------|--------------|------------------------------------|------------------|
| short int          | 2            | -32,768 to 32,767                 | %hd              |
| unsigned short int | 2            | 0 to 65,535                       | %hu              |
| unsigned int       | 4            | 0 to 4,294,967,295                | %u               |
| int                | 4            | -2,147,483,648 to 2,147,483,647   | %d               |
| long int           | 4            | -2,147,483,648 to 2,147,483,647   | %ld              |
| unsigned long int  | 4            | 0 to 4,294,967,295                | %lu              |
| long long int      | 8            | -(2^63) to (2^63)-1               | %lld             |
| unsigned long long int | 8        | 0 to 18,446,744,073,709,551,615   | %llu             |
| signed char        | 1            | -128 to 127                       | %c               |
| unsigned char      | 1            | 0 to 255                          | %c               |
| float              | 4            | 1.2E-38 to 3.4E+38                | %f               |
| double             | 8            | 1.7E-308 to 1.7E+308              | %lf              |
| long double        | 16           | 3.4E-4932 to 1.1E+4932            | %Lf              |

**Constants:** Declared with `const`, e.g., `const int MAX = 100`, unchangeable, useful for fixed values.

#### IO Operations
IO operations manage data exchange, primarily console-based in C. Key functions:
- **Output: printf()** from `<stdio.h>`, prints formatted output, e.g., `printf("Age: %d\n", age);` outputs "Age: 25" with newline. Format specifiers: `%d` (int), `%f` (float), `%c` (char), `%s` (string), `%lf` (double). Escape sequences: `\n` (newline), `\t` (tab).
- **Input: scanf()**, reads formatted input, e.g., `scanf("%d", &age);`, requires `&` for variable address. Can read multiple, e.g., `scanf("%d %f", &a, &b);`. Format specifiers match data types.

Other functions: `getchar()` reads single char, `putchar()` writes single char, `gets()` reads string (deprecated, use `fgets`), `puts()` writes string. `printf` returns characters printed, `scanf` returns items read, useful for error checking.

#### Operators and Expressions
Operators perform operations on operands, classified by functionality:
- **Arithmetic:** +, -, *, /, %, ++, --, unary +, unary -, e.g., `a + b`, `++i` increments.
- **Relational:** ==, !=, <, >, <=, >=, compare, return 1 (true) or 0 (false), e.g., `a == b`.
- **Logical:** && (AND, both true), || (OR, either true), ! (NOT, negates), e.g., `a && b`.
- **Bitwise:** &, |, ^, ~, <<, >>, operate on bits, e.g., `a & b` ANDs bits.
- **Assignment:** = (assign), +=, -=, *=, /=, %=, &=, |=, ^=, >>=, <<=, e.g., `a += 5`.
- **Other:** sizeof (size of type), comma (,), conditional (?:), dot (.) and arrow (->) for structures, cast for type conversion, & (addressof), * (dereference).

**Expressions:** Combinations like `a + b * c`, evaluated by precedence (e.g., * before +), associativity (left-to-right or right-to-left). Use parentheses for clarity, e.g., `(a + b) * c`.

#### Control Flow Statements
Control flow determines execution order, essential for logic:
- **Conditional:**
  - `if`: `if (condition) { code; }`, executes if true.
  - `if-else`: `if (condition) { } else { }`, chooses block.
  - `if-else-if`: Multiple conditions, e.g., `if (a>0) { } else if (a<0) { } else { }`.
  - `switch-case`: `switch (expr) { case val: code; break; default: code; }`, uses `break` to exit.
  - Ternary: `condition ? expr1 : expr2`, e.g., `a == 5 ? "equal" : "not equal"`.
- **Loops:**
  - `for`: `for(init; condition; inc) { code; }`, e.g., `for(int i=0; i<5; i++)`.
  - `while`: `while(condition) { code; }`, e.g., `while(count<5)`.
  - `do-while`: `do { code; } while(condition);`, executes at least once.
  - Nested: Loops within loops, e.g., for 2D arrays.
- **Jump:**
  - `break`: Exits loop/switch, e.g., `for(i=0; i<10; i++) { if(i==5) break; }`.
  - `continue`: Skips iteration, e.g., skips odd numbers.
  - `return`: Exits function, optionally returns, e.g., `return a+b;`.
  - `goto`: Jumps to label, e.g., `goto label; ... label: code;`, discouraged for readability.

#### Functions
Functions modularize code, reusable blocks performing tasks. Declare with `return_type name(parameter_list);`, define with body, e.g., `int add(int a, int b) { return a+b; }`. Call with `result = add(5, 6);`. Types: library (e.g., `printf`) and user-defined. Parameters pass by value (copy) or reference (pointers). Recursion: function calls itself, e.g., factorial. Return type can be `void` for no return, e.g., `void print() { printf("Hello"); }`.

#### Array
Arrays store same-type elements contiguously, declared as `data_type name[size];`, e.g., `int arr[5];`. Initialize `int arr[] = {1, 2, 3};`, access via index, e.g., `arr[0]`. Multi-dimensional, e.g., `int matrix[2][3]` for 2D. Passed to functions as pointers, e.g., `void print(int arr[], int size)`. Manage bounds to avoid overflow, e.g., accessing `arr[5]` in size 5 array is undefined.

#### Pointers
Pointers store addresses, declared as `data_type *name;`, e.g., `int *ptr;`. Initialize with `ptr = &var;`, dereference with `*ptr` for value. Used for dynamic memory (`malloc`, `free`), passing by reference, array access. Arithmetic: `ptr++` moves to next element, based on type size. Concepts: null pointer (points to 0), dangling (points to freed memory), pointer-to-pointer (`int **ptr`) for complex data.

#### String Handling
Strings are char arrays ending with '\0', declared as `char str[10];` or `char *str = "Hello";`. Handle with `<string.h>`: `strlen(str)` for length, `strcpy(dest, src)` for copy, `strcat(dest, src)` for concatenation, `strcmp(str1, str2)` for comparison (0 if equal). Ensure null terminator for proper handling, e.g., `char str[] = "Hello\0";`.

#### Structures and Unions
- **Structures:** Group different types, e.g., `struct Student { char name[50]; int age; };`. Declare variable `struct Student s;`, access with dot, e.g., `s.age = 20`. Useful for complex data like records.
- **Unions:** Share memory, e.g., `union Data { int i; float f; };`. Only one member active, e.g., if `i` set, `f` undefined. Saves space, useful for type-agnostic storage.

#### Files Handling
File handling reads/writes external files, using `<stdio.h>`. Open with `fopen("file.txt", "r")` for read, "w" for write, "a" for append. Close with `fclose(fp)`. Read/write with `fread`, `fwrite` for binary, `fprintf`, `fscanf` for formatted, e.g., `fprintf(fp, "%d", num);`. Check success, e.g., `if (fp == NULL) printf("Error opening file");`.

#### Pre-Processor Directives
Pre-process before compilation, starting with `#`. Include headers with `#include <stdio.h>` or `"header.h"`. Define macros with `#define PI 3.14`, e.g., `circum = 2 * PI * r;`. Conditional compilation: `#if`, `#ifdef`, `#ifndef`, `#else`, `#endif`, e.g., `#ifdef DEBUG printf("Debug mode"); #endif`. Enhances portability, code management.

#### Command Line Arguments
Pass inputs at execution, accessed via `main(int argc, char *argv[])`. `argc` is count, `argv` is string array. Example: `./program 10 20` has `argc=3`, `argv[0]="./program"`, `argv[1]="10"`, `argv[2]="20"`. Useful for flexible programs, e.g., file processing, configuration.

### Key Citations
- [Data Types in C GeeksforGeeks](https://www.geeksforgeeks.org/data-types-in-c/)
- [Variables in C GeeksforGeeks](https://www.geeksforgeeks.org/variables-in-c/)
- [Basic Input and Output in C GeeksforGeeks](https://www.geeksforgeeks.org/basic-input-and-output-in-c/)
- [Operators in C GeeksforGeeks](https://www.geeksforgeeks.org/operators-in-c/)
- [Control Flow Statements in Programming GeeksforGeeks](https://www.geeksforgeeks.org/control-flow-statements-in-programming/)
