# C Language QUIZ

Date: May 06, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

---

1. **Question:** What does the following declaration indicate?
   ```c
   int x: 8;
   ```
   - A. x stores a value of 8
   - B. x is an 8-bit integer
   - C. Both A and B
   - D. None of the above

   **Correct Answer:** B. x is an 8-bit integer
   
   **Explanation:** This declaration specifies that variable x is an 8-bit integer. The ": 8" part indicates the number of bits reserved for storing the value of x.

2. **Question:** Which of the following function is used to find the first occurrence of a given substring within a string?
   - A. strchr()
   - B. strrchr()
   - C. strstr()
   - D. strnset()

   **Correct Answer:** C. strstr()
   
   **Explanation:** The `strstr()` function is used to find the first occurrence of a given substring within a string in C.

3. **Question:** Which of the following are not standard header files in C?
   - A. stdio.h
   - B. stdlib.h
   - C. conio.h
   - D. None of the above

   **Correct Answer:** C. conio.h
   
   **Explanation:** Among the options provided, "conio.h" is not a standard header file in C. It is specific to DOS and Windows environments and provides functions for console input and output.

4. **Question:** What will be the output of the program?
   ```c
   #include <stdio.h>
   int main() {
       int x = 55;
       printf("%d, %d, %d",x<=55, x=40, x>=10);
       return 0;
   }
   ```
   - A. 1, 40, 1
   - B. 55, 55, 55
   - C. 55, 40, 10
   - D. Runtime error

   **Correct Answer:** A. 1, 40, 1
   
   **Explanation:** The code prints the results of three expressions separated by commas. The first expression `x<=55` evaluates to 1 because x is equal to 55. The second expression `x=40` assigns the value 40 to x and also returns the value of the assignment, which is 40. The third expression `x>=10` evaluates to 1 because x is now 40, which is greater than or equal to 10.

5. **Question:** What does the following declaration mean?
   ```c
   int (*ptr)[10];
   ```
   - A. ptr is array of pointers to 10 integers
   - B. ptr is a pointer to an array of 10 integers
   - C. ptr is an array of 10 integers
   - D. ptr is a pointer to array

   **Correct Answer:** B. ptr is a pointer to an array of 10 integers
   
   **Explanation:** This declaration indicates that ptr is a pointer to an array of 10 integers. The parentheses around `*ptr` indicate that ptr is a pointer, and `[10]` indicates that it's a pointer to an array of size 10.
