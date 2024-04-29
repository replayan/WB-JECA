# Data Structure QUIZ

Date: April 29, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

---

1. Which one of the following is the correct option to create a new node?
   - [ ] ptr= (node*)malloc(sizeof(node*))
   - [ ] ptr=(node)malloc(sizeof(node))
   - [x] ptr=(node*)malloc(sizeof(node))
   - [ ] None of the above

   **Correct Answer:** ptr=(node*)malloc(sizeof(node))

   **Explanation:** This option correctly allocates memory for a new node structure and returns a pointer to it.

2. The complexity of Bubble sort algorithm is
   - [ ] O(n)
   - [ ] O(log n)
   - [x] O(n^2)
   - [ ] O(n log n)

   **Correct Answer:** O(n^2)

   **Explanation:** Bubble Sort has a time complexity of O(n^2) due to its nested loop structure where each element is compared with every other element.

3. What is the asymptotic time complexity for adding a node at the end of a singly linked list, where the pointer is initially pointing to the head of the list?

    - [ ] O(1)
    - [x] O(n)
    - [ ] θ(n)
    - [ ] θ(1)

    **Explanation:**

    The correct answer is O(n).

    To add a new node at the end of a singly linked list, you need to traverse the list from the head until you reach the last node. In the worst-case scenario, when the list is not empty, you need to visit every node in the list to reach the last node.

    The number of operations required to traverse the list is directly proportional to the number of nodes in the list (n). Therefore, the time complexity of this operation is O(n), as the time taken grows linearly with the size of the input (the number of nodes in the list).

    The other options are not correct:

    - O(1) is not correct because, in the general case, you cannot add a node at the end of the list in constant time since you need to traverse the entire list.
    - θ(n) is not correct because it represents a tight bound, meaning the time complexity is both O(n) and Ω(n). However, in the best-case scenario, when the list is empty, you can add a new node as the head in constant time, which does not satisfy the Ω(n) condition.
    - θ(1) is not correct because it implies that the operation takes constant time, regardless of the input size, which is not the case for adding a node at the end of a singly linked list in the general case.

4. What are the number of moves required to solve the Tower of Hanoi problem for K disks?
   - [ ] 2K - 1
   - [ ] 2^k + 1
   - [ ] 2K + 1
   - [x] 2^k - 1

   **Correct Answer:** 2^k - 1

   **Explanation:** The number of moves required to solve the Tower of Hanoi problem for K disks is given by the formula 2^k - 1.

5. What determines the order of evaluation of a prefix expression?
   - [x] precedence and associativity
   - [ ] precedence only
   - [ ] associativity only
   - [ ] depends on the parser

   **Correct Answer:** precedence and associativity

   **Explanation:** In prefix expressions, the order of evaluation is primarily determined by the precedence and associativity of operators. However, the parser's implementation can also influence the order of evaluation, especially in ambiguous cases.
