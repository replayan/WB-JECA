# C lang QUIZ

Date: April 26, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

1. **What will be the output of the following C code?**

```c
#include <stdio.h>

void main() {
    int x = 1, y = 0, z = 5;
    int a = x && y || z++;
    printf("%d", z);
}
```

Options:
- A) 6
- B) 5
- C) 0
- D) varies

**Correct Answer: A) 6**

**Explanation:** 
The `z++` part of the expression `x && y || z++` will be evaluated because the logical AND (`&&`) operator short-circuits when the left operand is false. Hence, the value of `z` will be incremented before the print statement, resulting in the output `6`.

2. **The value returned by `func(435)` is:**

```c
int func(int num) {
    int count = 0;
    while (num) {
        count++;
        num >>= 1;
    }
    return (count);
}
```

Options:
- A) 9
- B) 10
- C) 11
- D) 8

**Correct Answer: A) 9**

**Explanation:**
The function `func` calculates the number of bits required to represent a given number `num` in binary. When `func(435)` is called, it returns 9 because 435 in binary requires 9 bits to represent (`110110011`).

3. **All keywords in C are in:**

Options:
- A) Lowercase letters
- B) Uppercase letters
- C) CamelCase letters
- D) None of the mentioned

**Correct Answer: A) Lowercase letters**

**Explanation:**
All keywords in C are in lowercase letters. Examples of keywords include `int`, `if`, `while`, `return`, etc.

4. **Which of the following are not standard header files in C?**

Options:
- A) stdio.h
- B) stdlib.h
- C) conio.h
- D) None of the above

**Correct Answer: C) conio.h**

**Explanation:**
The "conio.h" header file is not a standard header file in C. It's commonly used in MS-DOS and Windows programming environments for console input/output functions, but it's not part of the standard C library.

5. **What is the output of the C code?**

```c
#include <stdio.h>

int main() {
    int n;
    for (n = 7; n != 0; n--)
        printf("n = %d", n--);
    getchar();
    return 0;
}
```

Options:
- A) 7 6 5 4 3 2 1
- B) 6 4 2
- C) 7 5 3 2 1
- D) Infinite Loop

**Correct Answer: A) 7 6 5 4 3 2 1**

**Explanation:**
The loop starts with `n` initialized to 7. In each iteration, the value of `n` is printed, and then decremented by 2 (`n--` inside `printf` and `n--` in the loop condition). This results in printing the values of `n` starting from 7 and decrementing by 2 until it becomes 0, producing the output `7 6 5 4 3 2 1`.
