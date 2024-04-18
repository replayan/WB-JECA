1. **Which among the following can show polymorphism?**
   - ☐ Overloading &&
   - ✅ Overloading <<
   - ☐ Overloading ||
   - ☐ Overloading +=
   
   **Correct Answer:** Overloading <<

   **Explanation:** Overloading the `<<` operator, commonly used for output stream operations, can demonstrate polymorphism when used with polymorphic objects. It allows different types of objects to be printed using the same operator.

2. **Which of the following concepts means determining at runtime what method to invoke?**
   - ☐ Data hiding
   - ☐ Dynamic Typing
   - ✅ Dynamic binding
   - ☐ Dynamic loading
   
   **Correct Answer:** Dynamic binding
   
   **Explanation:** Dynamic binding, also known as late binding, allows the selection of the appropriate method or function to be called at runtime based on the actual type of the object. This enables polymorphic behavior.

3. **Which among the following is wrong syntax related to static data members?**
   - ☐ className :: staticDataMember;
   - ☐ dataType className :: memberName =value;
   - ☐ static dataType memberName;
   - ✅ className : dataType -> memberName;
   
   **Correct Answer:** `className : dataType -> memberName;`
   
   **Explanation:** This syntax is incorrect. The correct syntax for defining or declaring static data members in C++ does not use the colon and arrow symbols in this manner.

4. **Which of the following operators can be overloaded in C++?**
   - ✅ Member selection operator (.)
   - ☐ Size-of operator (sizeof)
   - ✅ Conditional operator (?:)
   - ☐ None of the above
   
   **Correct Answer:** Conditional operator (?:)
   
   **Explanation:** In C++, the conditional operator (?:) can be overloaded, allowing custom behavior to be defined for objects of user-defined types.

5. **Which of the following statements is correct in C++?**
   - ☐ Classes cannot have data as protected members.
   - ☐ Structures can have functions as members.
   - ☐ Class members are public by default.
   - ✅ Structure members are private by default.
   
   **Correct Answer:** Structure members are private by default.
   
   **Explanation:** In C++, if access modifiers are not explicitly specified, structure members are private by default. Similarly, for classes, members are private by default if access modifiers are not specified.