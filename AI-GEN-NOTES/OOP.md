# Object-Oriented Programming (OOP) in C++

## Basic Concepts

### Data Types
- **Primitive Types**: `int`, `char`, `float`, `double`, `bool`
- **Derived Types**: Arrays, Pointers, References
- **User-Defined Types**: `struct`, `class`, `enum`, `union`

### If / Else If / Else
- **Syntax**:
  ```cpp
  if (condition) {
      // statements
  } else if (another_condition) {
      // statements
  } else {
      // statements
  }
  ```

### Loops
- **For Loop**:
  ```cpp
  for (int i = 0; i < 10; ++i) {
      // statements
  }
  ```
- **While Loop**:
  ```cpp
  while (condition) {
      // statements
  }
  ```
- **Do-While Loop**:
  ```cpp
  do {
      // statements
  } while (condition);
  ```

### Functions
- **Syntax**:
  ```cpp
  return_type function_name(parameters) {
      // statements
      return value;
  }
  ```
- **Example**:
  ```cpp
  int add(int a, int b) {
      return a + b;
  }
  ```

### Switch Case
- **Syntax**:
  ```cpp
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

### Pointers
- **Definition**: Variables that store the memory address of another variable.
- **Syntax**:
  ```cpp
  int *ptr;
  int value = 10;
  ptr = &value;
  ```

### Structure
- **Definition**: User-defined data type that groups related variables.
- **Syntax**:
  ```cpp
  struct Person {
      string name;
      int age;
  };
  ```

### Array
- **Definition**: Collection of elements of the same type.
- **Syntax**:
  ```cpp
  int arr[5] = {1, 2, 3, 4, 5};
  ```

### String
- **Definition**: Sequence of characters.
- **Syntax**:
  ```cpp
  string str = "Hello, World!";
  ```

### Function Overloading
- **Definition**: Multiple functions with the same name but different parameters.
- **Example**:
  ```cpp
  int add(int a, int b) {
      return a + b;
  }

  double add(double a, double b) {
      return a + b;
  }
  ```

### Function Templates
- **Definition**: Functions that operate with generic types.
- **Syntax**:
  ```cpp
  template <typename T>
  T add(T a, T b) {
      return a + b;
  }
  ```

### SCOPE of Variable
- **Local Scope**: Variable declared inside a function or block.
- **Global Scope**: Variable declared outside all functions.

### Type Aliases (typedef / using)
- **typedef**: 
  ```cpp
  typedef unsigned long ulong;
  ```
- **using**:
  ```cpp
  using ulong = unsigned long;
  ```

### Unions
- **Definition**: User-defined data type where all members share the same memory location.
- **Syntax**:
  ```cpp
  union Data {
      int i;
      float f;
      char c;
  };
  ```

### Enumerated Types (enum)
- **Definition**: User-defined type consisting of a set of named integral constants.
- **Syntax**:
  ```cpp
  enum Color { RED, GREEN, BLUE };
  ```

## Classes and Object-Oriented Concepts

### Class
- **Definition**: Blueprint for creating objects.
- **Syntax**:
  ```cpp
  class ClassName {
  public:
      // member variables
      // member functions
  };
  ```

### Constructors
- **Definition**: Special member function called when an object is instantiated.
- **Syntax**:
  ```cpp
  ClassName() {
      // constructor body
  }
  ```

### Overloading Constructors
- **Definition**: Multiple constructors with different parameters.
- **Example**:
  ```cpp
  class Box {
  public:
      Box() {}
      Box(double l, double w, double h) : length(l), width(w), height(h) {}
  private:
      double length, width, height;
  };
  ```

### Member Initialization in Constructors
- **Syntax**:
  ```cpp
  ClassName() : member1(value1), member2(value2) {
      // constructor body
  }
  ```

### Pointers to Classes
- **Syntax**:
  ```cpp
  ClassName *ptr = new ClassName();
  delete ptr;
  ```

### Overloading Operators
- **Definition**: Providing a special meaning to an operator.
- **Syntax**:
  ```cpp
  class Complex {
  public:
      Complex operator + (const Complex &obj) {
          Complex res;
          res.real = this->real + obj.real;
          res.imag = this->imag + obj.imag;
          return res;
      }
  private:
      int real, imag;
  };
  ```

### Keyword `this`
- **Definition**: Pointer to the current object.
- **Usage**:
  ```cpp
  this->member = value;
  ```

### Static Members
- **Definition**: Members shared by all objects of the class.
- **Syntax**:
  ```cpp
  class ClassName {
  public:
      static int staticMember;
  };
  int ClassName::staticMember = 0;
  ```

### Const Member Functions
- **Definition**: Functions that do not modify the object.
- **Syntax**:
  ```cpp
  class ClassName {
  public:
      void display() const {
          // cannot modify any member variables
      }
  };
  ```

### Class Templates
- **Definition**: Classes that operate with generic types.
- **Syntax**:
  ```cpp
  template <typename T>
  class ClassName {
  private:
      T member;
  public:
      ClassName(T arg) : member(arg) {}
  };
  ```

### Template Specialization
- **Definition**: Specializing a template for a specific type.
- **Syntax**:
  ```cpp
  template <>
  class ClassName<int> {
  private:
      int member;
  public:
      ClassName(int arg) : member(arg) {}
  };
  ```

### Namespace
- **Definition**: Logical grouping of related classes, functions, and variables.
- **Syntax**:
  ```cpp
  namespace MyNamespace {
      int var;
      void func() {}
  }
  ```

Sure, let me include the definitions for Friend Functions and Friend Classes along with examples for clarity.

---

### Friend Functions
- **Definition**: A friend function is a function that is not a member of a class but has access to the class's private and protected members.
- **Usage**: Used to allow an external function to access the private and protected data of a class.
- **Syntax**:
  ```cpp
  class ClassName {
  private:
      int data;
  public:
      ClassName() : data(0) {}
      // Friend function declaration
      friend void friendFunction(ClassName &obj);
  };

  // Friend function definition
  void friendFunction(ClassName &obj) {
      obj.data = 10; // Accessing private member
      std::cout << "Data: " << obj.data << std::endl;
  }
  ```

### Friend Classes
- **Definition**: A friend class is a class that has access to the private and protected members of another class.
- **Usage**: Used to allow all member functions of one class to access the private and protected data of another class.
- **Syntax**:
  ```cpp
  class B; // Forward declaration

  class A {
  private:
      int data;
  public:
      A() : data(0) {}
      // Friend class declaration
      friend class B;
  };

  class B {
  public:
      void accessA(A &obj) {
          obj.data = 20; // Accessing private member of A
          std::cout << "Data: " << obj.data << std::endl;
      }
  };
  ```

## Example Illustrations

### Example of Friend Function
```cpp
#include <iostream>

class Box {
private:
    double width;
public:
    Box() : width(0) {}
    // Friend function
    friend void setWidth(Box &b, double w);
};

void setWidth(Box &b, double w) {
    b.width = w; // Accessing private member
    std::cout << "Width: " << b.width << std::endl;
}

int main() {
    Box box;
    setWidth(box, 10.5);
    return 0;
}
```
**Output**:
```
Width: 10.5
```

### Example of Friend Class
```cpp
#include <iostream>

class Rectangle;

class Square {
private:
    int side;
public:
    Square(int s) : side(s) {}
    // Friend class declaration
    friend class Rectangle;
};

class Rectangle {
public:
    int area(Square &sq) {
        return sq.side * sq.side; // Accessing private member of Square
    }
};

int main() {
    Square sq(4);
    Rectangle rect;
    std::cout << "Area: " << rect.area(sq) << std::endl;
    return 0;
}
```
**Output**:
```
Area: 16
```

### Inheritance
- **Definition**: Mechanism for creating a new class from an existing class.
- **Syntax**:
  ```cpp
  class Derived : public Base {
  };
  ```

### Polymorphism
- **Definition**: Ability to call derived class methods through a base class reference.
- **Example**:
  ```cpp
  class Base {
  public:
      virtual void show() {
          cout << "Base show" << endl;
      }
  };
  class Derived : public Base {
  public:
      void show() override {
          cout << "Derived show" << endl;
      }
  };
  Base *b = new Derived();
  b->show(); // Output: Derived show
  ```

### Virtual Members
- **Definition**: Functions that can be overridden in derived classes.
- **Syntax**:
  ```cpp
  class Base {
  public:
      virtual void display() {
          cout << "Display Base" << endl;
      }
  };
  ```

### Abstract Base Class
- **Definition**: Class that cannot be instantiated and often contains pure virtual functions.
- **Syntax**:
  ```cpp
  class AbstractBase {
  public:
      virtual void pureVirtualFunction() = 0; // Pure virtual function
  };
  ```
