1. Which of the following operators has the lowest precedence?
   - [ ] `!=`
   - [ ] `&&`
   - [ ] `?:`
   - [x] `,`
   
   Explanation: The comma operator (`,`) typically has the lowest precedence. It evaluates each of its operands (from left to right) and returns the value of the last operand.

2. What does the following declaration mean?
   `int (*ptr)[10];`
   - [ ] `ptr` is an array of pointers to 10 integers.
   - [x] `ptr` is a pointer to an array of 10 integers.
   - [ ] `ptr` is an array of 10 integers.
   - [ ] `ptr` is a pointer to array.

   Explanation: The declaration `int (*ptr)[10];` means that `ptr` is a pointer to an array of 10 integers.

3. Which of the following is not a storage class specifier in C?
   - [ ] `auto`
   - [ ] `register`
   - [ ] `static`
   - [x] `volatile`
   
   Explanation: The `volatile` keyword is not a storage class specifier in C; it's a type qualifier that indicates that an object may be changed by something external to the program.

4. What will be the output of the following C code?
   ```c
   #include <stdio.h>
   int main() {
       int i = 0;
       int x = i++, y = ++i;
       printf("%d % d\n", x, y);
       return 0;
   }
   ```
   - [x] `0, 2`
   - [ ] `0, 1`
   - [ ] `1, 2`
   - [ ] Compile time error

   Explanation: There's a space in the format string `%d % d`, which may lead to unexpected output. However, this doesn't cause a compile-time error. The correct output is `0 2`, as `x` gets the value 0 and `y` gets the value 2.

5. What is the purpose of the `volatile` keyword in C?
   - [ ] It specifies that a variable cannot be modified after it's declared.
   - [ ] It specifies that a variable cannot be accessed by multiple threads simultaneously.
   - [ ] It specifies that a variable's value should be cached for faster access.
   - [x] It specifies that an object may be changed by something external to the program.
   
   Explanation: The `volatile` keyword indicates that an object may be changed by something external to the program, such as hardware or another thread, and it prevents the compiler from applying certain optimizations that assume the value of the object cannot change unexpectedly.
