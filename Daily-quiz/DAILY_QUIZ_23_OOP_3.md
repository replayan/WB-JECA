# OOPs QUIZ

Date: May 17, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

---

## Multiple Choice Questions:

**Question 1: Which of the following statements is correct in C++?**

**Options:**

- Classes cannot have data as protected members.
- Structures can have functions as members. **(Correct)**
- Class members are public by default.
- Structure members are private by default.

**Explanation:**

- In C++, classes and structures are similar constructs for defining user-defined data types.
- The key difference lies in the default member access specifiers:
    - **Class members are private by default.** You can explicitly make them `public` or `protected` if needed.
    - **Structure members are public by default.** You can explicitly make them `private` if needed.
- While classes cannot have protected data members directly, they can achieve similar behavior using inheritance and protected members in the base class.
- Structures, on the other hand, can have functions (methods) as members.

**Question 2: What is the output of the following program?**

```c++
#include <iostream>
using namespace std;

int main() {
    int var = 0;
    while (var < 10) {
        cout << var << " ";
        var++;
    }
    cout << var << endl;
    return 0;
}
```

**Options:**

- 0 1 2 3 4 5 6 7 8 9 10
- 0 1 2 3 4 5 6 7 8 9
- 1 2 3 4 5 6 7 8 9 10
- 1 2 3 4 5 6 7 8 9

**Correct Answer:**

- 0 1 2 3 4 5 6 7 8 9 10

**Explanation:**

The code iterates 10 times, printing the value of `var` followed by a space in each iteration. The final newline (`endl`) is added after the loop completes.

**Question 3: Which is the correct syntax for using default arguments with the constructor?**

**Options:**

- `default constructorName(default int x = 0)` (Incorrect)
- `constructorName(default int x = 0)` (Incorrect)
- `constructorName(int x = 0)` (Correct)
- `constructorName()` (Incorrect)

**Explanation:**

The correct syntax is `constructorName(int x = 0)`. This defines a constructor that takes an optional integer parameter `x`. If no argument is provided when calling the constructor, `x` will be initialized to the default value of 0.

**Question 4: What is `iostream` stream class?**

**Options:**

- `iostream` class inherits the properties of `ios`. (Correct)
- `iosstream` class inherits the properties of only `istream`. (Incorrect)
- `iosstream` class inherits the properties of `istream` and `ostream`. (Correct) (Alternative wording)
- `iosstream` class inherits the properties of only `ostream`. (Incorrect)

**Explanation:**

- The `iostream` class inherits from the `ios` base class, gaining basic stream properties and functionalities.
- It further inherits from both `istream` and `ostream`, enabling it to perform both input and output operations.

**Question 5: Which inheritance type is used in the class given below?**

```c++
class A : public X, public Y
{}
```

**Options:**

- Multiple inheritance (Correct)
- Multilevel inheritance (Incorrect)
- Hybrid inheritance (Incorrect)
- Hierarchical inheritance (Incorrect)

**Explanation:**

The class `A` directly inherits from two base classes, `X` and `Y`. This is the defining characteristic of **multiple inheritance**.
