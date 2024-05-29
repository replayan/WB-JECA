# Data Structures and Algorithms QUIZ

Date: May 29, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

---

### 1. What is the worst case complexity of printing the elements of a binary search tree in sorted order?
- **O(n²)**
- **O(log n)**
- **O(n)**
- **O(n logn)**

**Correct Answer:** O(n)

**Explanation:** To print the elements of a BST in sorted order, an in-order traversal is performed. Each node is visited exactly once, resulting in a time complexity of O(n), where n is the number of nodes in the tree.

---

### 2. The equivalent infix expression and value for the postfix form `1 2 + 3 * 4 5 * –` will be ___________.
- **1 + 2 * 3 – 4 * 5 and -13**
- **(2 + 1) * (3 – 4) * 5 and -15**
- **1 + 2 * (3 – 4) * 5 and -9**
- **(1 + 2) * 3 – (4 * 5) and -11**

**Correct Answer:** (1 + 2) * 3 – (4 * 5) and -11

**Explanation:** The postfix expression `1 2 + 3 * 4 5 * –` translates to the infix expression `((1 + 2) * 3) – (4 * 5)`. Evaluating this expression step-by-step gives the result -11.

---

### 3. In the worst case, the number of comparisons needed to search a singly linked list of length n for a given element is?
- **log₂ n**
- **n/2**
- **log₂ n – 1**
- **n**

**Correct Answer:** n

**Explanation:** In the worst case, to find a specific element or determine that it is not present in a singly linked list, you must traverse and compare each of the n nodes. This results in n comparisons.

---

### 4. In a binary search tree data structure, in-order traversal means the nodes are being searched in ______ order.
- **left child node - right child node - root node**
- **right child node - root node - left child node**
- **root node - right child node - left child node**
- **left child node - root node - right child node**

**Correct Answer:** left child node - root node - right child node

**Explanation:** In-order traversal of a binary search tree visits the left subtree first, then the root node, and finally the right subtree. This traversal results in visiting the nodes in sorted order.

---

### 5. For the quicksort algorithm, what is the time complexity of the best/worst case?
- **best case: O(n) worst case: O(n²)**
- **best case: O(n) worst case: O(n log n)**
- **best case: O(n log n) worst case: O(n log n)**
- **best case: O(n log n) worst case: O(n²)**

**Correct Answer:** best case: O(n log n) worst case: O(n²)

**Explanation:** The best case for quicksort occurs when the pivot divides the array into two nearly equal halves at each step, leading to a time complexity of O(n log n). The worst case occurs when the pivot results in the most unbalanced partitions, leading to a time complexity of O(n²).
