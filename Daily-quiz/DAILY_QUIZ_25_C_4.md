# C language QUIZ

Date: May 26, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

---

### 1. What is the output of the following program?
```c
#include <stdio.h>
int main()
{
    int i = 3;
    printf("%d", (++i)++);
    return 0;
}
```
- a) 3
- b) 4
- c) 5
- d) Compile-time error

**Answer**: d) Compile-time error

**Explanation**: The expression `(++i)++` is attempting to apply the post-increment operator to the result of a pre-increment operation, which is not allowed by the C standard. The compiler will produce an error indicating that the operand of `++` must be a modifiable lvalue.

---

### 2. What will be the output of the program?
```c
#include <stdio.h>
int main() {
    printf("%d", printf("JECA"));
    return 0;
}
```
- a) JECA4
- b) Garbage value
- c) Syntax error
- d) Display JECA and terminate

**Answer**: a) JECA4

**Explanation**: The inner `printf("JECA")` prints "JECA" and returns the number of characters printed, which is 4. The outer `printf` then prints this value, resulting in "JECA4".

---

### 3. What will be the output of the program?
```c
#include <stdio.h>
int main() {
    int i = -3, j = 2, k = 0, m;
    m = ++i && ++j && ++k;
    printf("%d, %d, %d, %d\n", i, j, k, m);
}
```
- a) -2, 3, 1, 1
- b) 2, 3, 1, 2
- c) 1, 2, 3, 1
- d) 3, 3, 1, 2

**Answer**: a) -2, 3, 1, 1

**Explanation**: The variables `i`, `j`, and `k` are pre-incremented, resulting in `i = -2`, `j = 3`, and `k = 1`. Since all pre-increment results are non-zero (true), `m` is set to `1`.

---

### 4. The value returned by `func(435)` is:
```c
int func(int num)
{
    int count = 0;
    while (num)
    {
        count++;
        num >>= 1;
    }
    return (count);
}
```
- a) 9
- b) 10
- c) 11
- d) 8

**Answer**: a) 9

**Explanation**: The function counts the number of times the integer `435` can be right-shifted until it becomes zero. The binary representation of `435` is `110110011` (9 bits), so the function returns `9`.

---

### 5. What is the result of logical or relational expression in C?
- a) True or False
- b) 0 or 1
- c) 0 if an expression is false and any positive number if an expression is true
- d) None of the mentioned

**Answer**: b) 0 or 1

**Explanation**: In C, logical and relational expressions evaluate to `0` (false) or `1` (true). This is consistent across all such expressions, ensuring clear and predictable results.
