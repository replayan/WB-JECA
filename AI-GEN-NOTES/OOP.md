# OOPs Concept's

---

## 1. Data Types

### Primitive Data Types
- **Integer types:** `int`, `short`, `long`, `unsigned int`, etc.
- **Floating-point types:** `float`, `double`, `long double`
- **Character type:** `char`
- **Boolean type (C++):** `bool`

### Derived Data Types
- **Pointers:** Variables that hold memory addresses.
- **Arrays:** Collections of elements of the same type.
- **Functions:** Blocks of code that perform tasks.
- **References (in C++):** Alias for another variable.

### User-Defined Data Types
- **Structures (struct):** Collection of variables under one name.
- **Unions:** Special structure where all members share the same memory.
- **Enumerated types (enum):** User-defined type consisting of named constants.
- **Classes:** Blueprint for objects combining data and functions.

---

## 2. Control Structures

### If / Else If / Else
- **If Statement:** Executes a block of code if a condition is true.
  
  ```cpp
  if (condition) {
      // code if condition is true
  } else if (another_condition) {
      // code if the second condition is true
  } else {
      // code if none of the above conditions are met
  }
  ```

- **Key Points:**  
  - Conditions are typically expressions that evaluate to true/false.
  - Can be nested for more complex decisions.

### Switch Case
- **Definition:** A multi-way branch statement.
  
  ```cpp
  switch (variable) {
      case value1:
          // code for value1
          break;
      case value2:
          // code for value2
          break;
      default:
          // default case code
  }
  ```

- **Key Points:**  
  - Evaluates an expression once and compares it against constant values.
  - `break` prevents fall-through; without it, execution continues into the next case.

---

## 3. Loops

### For Loop
- **Structure:**
  
  ```cpp
  for (initialization; condition; update) {
      // loop body
  }
  ```

- **When to Use:** Iterating when the number of iterations is known.

### While Loop
- **Structure:**
  
  ```cpp
  while (condition) {
      // loop body
  }
  ```

- **When to Use:** When the condition is checked before the loop starts.

### Do-While Loop
- **Structure:**
  
  ```cpp
  do {
      // loop body
  } while (condition);
  ```

- **When to Use:** Ensures the loop runs at least once.

---

## 4. Functions

### Definition and Declaration
- **Definition:** A block of code that performs a specific task.
- **Declaration/Prototype:** Tells the compiler about the function name, return type, and parameters.
  
  ```cpp
  // Declaration (prototype)
  int add(int a, int b);

  // Definition
  int add(int a, int b) {
      return a + b;
  }
  ```

- **Key Points:**  
  - Promote code reusability.
  - Functions can return values or be void (no return value).

---

## 5. Pointers

### Definition
- **Concept:** Variables that store memory addresses of other variables.
- **Syntax Example:**
  
  ```cpp
  int a = 10;
  int *ptr = &a;  // ptr stores the address of a
  ```

### Key Points:
- **Dereferencing:** Using `*ptr` to access the value.
- **Pointer Arithmetic:** Incrementing pointers to traverse arrays.
- **Null Pointers:** Use `nullptr` (C++) or `NULL` (C) when a pointer does not reference a valid memory location.

---

## 6. Structures

### Definition
- **Structures (struct):** Custom data types that group variables.
  
  ```cpp
  struct Point {
      int x;
      int y;
  };

  Point p1 = {10, 20};
  ```

### Key Points:
- Useful for modeling records (e.g., a student’s record).
- Members are by default public (in C++ structs).

---

## 7. Arrays

### Definition
- **Array:** A collection of elements of the same type stored in contiguous memory.
  
  ```cpp
  int arr[5] = {1, 2, 3, 4, 5};
  ```

### Key Points:
- Fixed size once declared.
- Indexing starts at 0.
- Can be multi-dimensional (e.g., matrices).

---

## 8. Strings

### C-Style Strings
- **Definition:** Arrays of characters ending in a null character (`'\0'`).
  
  ```cpp
  char str[] = "Hello";
  ```

### C++ `std::string`
- **Definition:** A more flexible string class provided by the C++ Standard Library.
  
  ```cpp
  #include <string>
  std::string greeting = "Hello";
  ```

### Key Points:
- `std::string` supports numerous operations like concatenation, substring extraction, and length calculation.

---

## 9. Function Overloading

### Definition
- **Concept:** Multiple functions can have the same name but different parameter lists.
  
  ```cpp
  int add(int a, int b) { return a + b; }
  double add(double a, double b) { return a + b; }
  ```

### Key Points:
- Determined by the number, order, and types of parameters.
- Improves code readability and usability.

---

## 10. Function Templates

### Definition
- **Concept:** Write generic functions that work with different data types.
  
  ```cpp
  template <typename T>
  T add(T a, T b) {
      return a + b;
  }
  ```

### Key Points:
- Helps in code reusability.
- The compiler generates the function code for each type it is used with.

---

## 11. Scope of Variables

### Local Scope
- **Definition:** Variables declared inside a function/block; accessible only within that block.

### Global Scope
- **Definition:** Variables declared outside any function; accessible from any part of the program.

### Block Scope (C++ Specific)
- **Definition:** Variables declared inside `{ }` (e.g., in loops or conditional blocks).

### Key Points:
- Variables are only accessible within the region they are declared.
- Shadowing can occur when a local variable has the same name as a global variable.

---

## 12. Type Aliases (typedef / using)

### typedef
- **Syntax:**
  
  ```cpp
  typedef unsigned long ulong;
  ulong myVar = 100;
  ```

### using (C++11 onwards)
- **Syntax:**
  
  ```cpp
  using ulong = unsigned long;
  ulong myVar = 100;
  ```

### Key Points:
- Improve code readability.
- Helpful in simplifying complex type definitions.

---

## 13. Unions

### Definition
- **Concept:** A union allows different data types to share the same memory location.
  
  ```cpp
  union Data {
      int i;
      float f;
      char str[20];
  };
  ```

### Key Points:
- Only one member can contain a value at any one time.
- Useful when storing one of several types of data in the same memory space.

---

## 14. Enumerated Types (enum)

### Definition
- **Concept:** Creates a new type with a set of named integer constants.
  
  ```cpp
  enum Color { RED, GREEN, BLUE };
  Color c = RED;
  ```

### Key Points:
- Improves code clarity by using symbolic names.
- Underlying type is usually `int` (modifiable in C++11 with enum class).

---

## 15. Classes

### Definition
- **Class:** A blueprint for creating objects, encapsulating data and behaviors.
  
  ```cpp
  class Rectangle {
  private:
      int width, height;

  public:
      void setDimensions(int w, int h) {
          width = w;
          height = h;
      }
      int area() {
          return width * height;
      }
  };
  ```

### Key Points:
- Encapsulation, data hiding, and abstraction are key principles.
- Members can be `private`, `protected`, or `public`.

---

## 16. Constructors

### Definition
- **Constructors:** Special member functions automatically called when an object is created.
  
  ```cpp
  class Rectangle {
  public:
      int width, height;
      // Default constructor
      Rectangle() : width(0), height(0) {}

      // Parameterized constructor
      Rectangle(int w, int h) : width(w), height(h) {}
  };
  ```

### Key Points:
- **Default constructor:** No parameters.
- **Parameterized constructor:** Takes arguments for initialization.
- Automatically initialize data members.

---

## 17. Overloading Constructors

### Definition
- **Concept:** Provide multiple constructors with different parameters.
  
  ```cpp
  class Point {
  public:
      int x, y;
      // Default constructor
      Point() : x(0), y(0) {}

      // Parameterized constructor
      Point(int a, int b) : x(a), y(b) {}
  };
  ```

### Key Points:
- Offers flexibility when initializing objects.
- Each constructor may handle a different initialization scenario.

---

## 18. Member Initialization in Constructors

### Definition
- **Member Initialization List:** A list used in constructors to initialize class members before the constructor body runs.
  
  ```cpp
  class Person {
      std::string name;
      int age;
  public:
      Person(const std::string &n, int a) : name(n), age(a) {}
  };
  ```

### Key Points:
- Essential for initializing const members or reference members.
- More efficient when initializing complex data types.

---

## 19. Pointers to Classes

### Definition
- **Concept:** Pointers can point to objects, enabling dynamic allocation and polymorphism.
  
  ```cpp
  class MyClass { /* ... */ };
  MyClass* objPtr = new MyClass();
  // Access members using the arrow operator: objPtr->memberFunction();
  delete objPtr;
  ```

### Key Points:
- Useful in dynamic memory allocation and managing object lifetimes.
- Facilitate runtime polymorphism when used with virtual functions.

---

## 20. Overloading Operators

### Definition
- **Concept:** Redefine the meaning of an operator for user-defined classes.
  
  ```cpp
  class Complex {
      float real, imag;
  public:
      Complex(float r = 0, float i = 0) : real(r), imag(i) {}
      // Overload the '+' operator
      Complex operator + (const Complex &c) const {
          return Complex(real + c.real, imag + c.imag);
      }
  };
  ```

### Key Points:
- Increases the readability of code that uses class objects.
- Both member operator overloads and friend function overloads can be implemented.

---

## 21. Keyword `this`

### Definition
- **Concept:** A pointer that holds the address of the current object.
  
  ```cpp
  class Box {
      int length;
  public:
      Box(int l) { this->length = l; }
  };
  ```

### Key Points:
- Used to avoid naming conflicts.
- It can also be used to return the calling object (e.g., in chained calls).

---

## 22. Static Members

### Definition
- **Static Data Members:** Shared across all instances of a class.
- **Static Member Functions:** Can be called on the class itself rather than on an instance.
  
  ```cpp
  class Counter {
  public:
      static int count;
      Counter() { count++; }
      static int getCount() { return count; }
  };

  int Counter::count = 0; // Definition outside the class
  ```

### Key Points:
- Static members have a single copy shared by all objects.
- Useful for counters, configuration values, or shared resources.

---

## 23. Const Member Functions

### Definition
- **Const Member Functions:** Promises not to modify any member variables (except those declared mutable) of the object.
  
  ```cpp
  class Sample {
      int value;
  public:
      Sample(int val) : value(val) {}
      int getValue() const { return value; }
  };
  ```

### Key Points:
- Enforced by the compiler to improve code safety.
- Allow calling these functions on const-qualified objects.

---

## 24. Class Templates

### Definition
- **Concept:** Create classes that work with any data type.
  
  ```cpp
  template <typename T>
  class Stack {
      std::vector<T> elems;
  public:
      void push(const T &elem) { elems.push_back(elem); }
      T pop() {
          T topElem = elems.back();
          elems.pop_back();
          return topElem;
      }
  };
  ```

### Key Points:
- Enables generic programming.
- The class is instantiated with a specific type when used.

---

## 25. Template Specialization

### Definition
- **Concept:** Customizing the behavior of a template for a specific type.
  
  ```cpp
  template <typename T>
  class Printer {
  public:
      void print(const T &data) { std::cout << data; }
  };

  // Template specialization for char*
  template <>
  class Printer<char*> {
  public:
      void print(char* const &data) { std::cout << "String: " << data; }
  };
  ```

### Key Points:
- Allows you to define a special case when the generic template does not suffice.
- Helps fine-tune behavior for specific data types.

---

## 26. Namespace

### Definition
- **Concept:** Provides a way to group related functions, classes, and variables to prevent name collisions.
  
  ```cpp
  namespace MathFunctions {
      int add(int a, int b) { return a + b; }
  }

  int main() {
      int sum = MathFunctions::add(3, 4);
      return 0;
  }
  ```

### Key Points:
- Useful in large projects to avoid identifier conflicts.
- The `using` directive can import all names or a specific name from a namespace.

---

## 27. Friendship (Friend Functions & Friend Classes)

### Friend Functions
- **Definition:** Non-member functions declared with `friend` inside a class so they can access private/protected members.
  
  ```cpp
  class Box {
      int width;
  public:
      Box(int w) : width(w) {}
      friend void printWidth(const Box&);
  };

  void printWidth(const Box &b) {
      std::cout << "Width: " << b.width;
  }
  ```

### Friend Classes
- **Definition:** A class declared as a friend of another class, hence its member functions have access to the private and protected members.
  
  ```cpp
  class A {
      int data;
  public:
      A(int d) : data(d) {}
      friend class B;
  };

  class B {
  public:
      void showData(A &a) {
          std::cout << "Data: " << a.data;
      }
  };
  ```

### Key Points:
- Friendship is not transitive nor reciprocal.
- Useful in operator overloading and when two or more classes need intimate access to each other’s data.

---

## 28. Inheritance

### Definition
- **Concept:** A mechanism where one class (derived class) inherits attributes and methods from another class (base class).
  
  ```cpp
  class Animal {
  public:
      void eat() { std::cout << "Eating"; }
  };

  class Dog : public Animal {
  public:
      void bark() { std::cout << "Barking"; }
  };
  ```

### Types of Inheritance:
- **Public:** Public and protected members of the base become public and protected members of the derived class.
- **Protected/Private Inheritance:** Base class members’ access levels are adjusted accordingly.

### Key Points:
- Facilitates code reuse.
- Supports hierarchical classification of classes.
- Base class pointers can refer to derived class objects (useful in polymorphism).

---

## 29. Polymorphism

### Definition
- **Concept:** The ability of a function or object to take on many forms.
- **Compile-Time Polymorphism:** Achieved with function overloading, operator overloading, and templates.
- **Run-Time Polymorphism:** Achieved with virtual functions.

### Key Points:
- Promotes flexibility and reuse.
- In C++, virtual functions allow derived class methods to override base class methods.

---

## 30. Virtual Members

### Definition
- **Virtual Functions:** Member functions declared with the `virtual` keyword so that they can be overridden in derived classes.
  
  ```cpp
  class Base {
  public:
      virtual void display() { std::cout << "Base display"; }
  };

  class Derived : public Base {
  public:
      void display() override { std::cout << "Derived display"; }
  };
  ```

### Key Points:
- Enables run-time (dynamic) polymorphism.
- Calls to virtual functions are resolved according to the actual object type pointed to, not the pointer type.

---

## 31. Abstract Base Class

### Definition
- **Concept:** A class that cannot be instantiated and is designed to be a base class.
- **Pure Virtual Functions:** Declared by assigning `= 0` to a virtual function.
  
  ```cpp
  class Shape {
  public:
      // Pure virtual function makes Shape an abstract class
      virtual void draw() = 0;
  };

  class Circle : public Shape {
  public:
      void draw() override { std::cout << "Drawing Circle"; }
  };
  ```

### Key Points:
- Enforces that derived classes implement certain functions.
- Useful when you want to define an interface that multiple derived classes must adhere to.

---

## Final Summary

- **Fundamentals:** Begin with understanding basic data types (primitive, derived, user-defined) and control structures like if/else, loops, and switch case.
- **Functions and Templates:** Grasp function declarations and definitions, overloading, and templates to enable generic programming.
- **Memory Management:** Emphasize pointers, structures, arrays, and strings—understanding how memory is allocated and accessed.
- **OOP Concepts:** Dive into class fundamentals including constructors (with overloading and member initialization), static members, const member functions, and the use of `this`.
- **Advanced Topics:** Study operator overloading, class templates, template specialization, namespaces, and friendship to enhance functionality.
- **Inheritance & Polymorphism:** Understand the principles of inheritance, polymorphism via virtual functions, and create abstract base classes for defining interfaces.
