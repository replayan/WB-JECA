# OOPs QUIZ

Date: June 16, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

---

## Multiple Choice Questions:

## Question 1
**Which of the following concepts means adding new components to a program as it runs?**
- [ ] Data hiding
- [ ] Dynamic typing
- [ ] Dynamic binding
- [x] Dynamic loading

**Explanation:**
Dynamic loading is a process where a program can load and link new modules or components while it is executing, rather than at compile time. This allows for more flexibility and can save memory by loading components only when they are needed.

## Question 2
**A non-member function cannot access which data of the class?**
- [x] Private data
- [ ] Public data
- [ ] Protected data
- [ ] All of the above

**Explanation:**
Non-member functions cannot access private and protected data of a class unless they are declared as friend functions. Public data, however, is accessible to non-member functions.

## Question 3
**What is the output of the following program?**

```cpp
#include <iostream>
using namespace std;

struct demo {
    int var;
};

int main() {
    demo str;
    demo *ptr;
    str.var = 100;
    ptr = &str;
    cout << ptr->var;
    return 0;
}
```

- [x] 100
- [ ] Memory address of var
- [ ] Compile Error
- [ ] L-value Error

**Explanation:**
The pointer `ptr` points to the object `str`, and `str.var` is set to 100. Therefore, `ptr->var` outputs the value of `str.var`, which is 100.

## Question 4
**What is the output of the following program?**

```cpp
#include <iostream>
using namespace std;

class Base {
public:
    void display() {
        cout << "[Base:display]";
    }
    virtual void print() {
        cout << "[Base:print]";
    }
};

class Derived : public Base {
public:
    void display() {
        cout << "[Derived:display]";
    }
    void print() {
        cout << "[Derived:print]";
    }
};

int main() {
    Base *p = new Derived();
    p->display();
    p->print();
    return 0;
}
```

- [ ] [Base:display][Base:print]
- [ ] [Derived:display][Derived:print]
- [ ] [Derived:display][Base:print]
- [x] [Base:display][Derived:print]

**Explanation:**
`p->display()` calls `Base::display()` because `display()` is not virtual and is resolved at compile time based on the pointer type `Base*`. `p->print()` calls `Derived::print()` because `print()` is virtual and is resolved at runtime based on the actual object type `Derived`.

## Question 5
**Which of the following type of class allows only one object of it to be created?**
- [ ] Virtual class
- [ ] Abstract class
- [ ] Friend class
- [x] Singleton class

**Explanation:**
A Singleton class ensures that only one instance of the class can be created. This design pattern restricts the instantiation of the class and provides a global point of access to the instance.
