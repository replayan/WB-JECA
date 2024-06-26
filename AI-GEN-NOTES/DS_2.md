## Data Structures

Data structures are ways of organizing and storing data in a computer program to efficiently manage and access the data. Some of the most commonly used data structures are:

### Searching and Sorting

**Searching**:
- **Linear Search**: Best case O(1), Average case O(n), Worst case O(n)
- **Binary Search**: Best case O(1), Average case O(log n), Worst case O(log n)

**Sorting**:
- **Bubble Sort**: Best case O(n), Average case O(n^2), Worst case O(n^2)
- **Insertion Sort**: Best case O(n), Average case O(n^2), Worst case O(n^2) 
- **Selection Sort**: Best case O(n^2), Average case O(n^2), Worst case O(n^2)
- **Merge Sort**: Best case O(n log n), Average case O(n log n), Worst case O(n log n)
- **Quick Sort**: Best case O(n log n), Average case O(n log n), Worst case O(n^2)
- **Heap Sort**: Best case O(n log n), Average case O(n log n), Worst case O(n log n)

### Stack
A stack is a linear data structure that follows the Last-In-First-Out (LIFO) principle. The main operations are:

- **Push**: Add an element to the top of the stack. Time complexity: O(1)
- **Pop**: Remove the top element from the stack. Time complexity: O(1) 
- **Peek**: Access the top element without removing it. Time complexity: O(1)
- **IsEmpty**: Check if the stack is empty. Time complexity: O(1)

Stacks have applications in expression evaluation, function calls, backtracking algorithms, and more.

### Queue
A queue is a linear data structure that follows the First-In-First-Out (FIFO) principle. The main operations are:

- **Enqueue**: Add an element to the rear of the queue. Time complexity: O(1)
- **Dequeue**: Remove the front element from the queue. Time complexity: O(1)
- **Peek**: Access the front element without removing it. Time complexity: O(1) 
- **IsEmpty**: Check if the queue is empty. Time complexity: O(1)

Queues have applications in job scheduling, breadth-first search, and more.

### Linked List
A linked list is a linear data structure where each element (called a node) contains a pointer to the next node in the list. The main operations are:

- **Insert**: Add a new node at the beginning, end, or a specific position. Time complexity: O(1) for beginning, O(n) for end/specific position
- **Delete**: Remove a node from the list. Time complexity: O(1) for beginning, O(n) for end/specific position
- **Search**: Find a node with a given value. Time complexity: O(n)

Linked lists are useful for implementing stacks, queues, and other data structures. They provide efficient insertion and deletion at the cost of slower access.

### Tree
A tree is a non-linear hierarchical data structure that consists of nodes connected by edges. Some common tree types are:

- **Binary Tree**: Each node has at most two child nodes. 
  - **Traversal**: Inorder, Preorder, Postorder. Time complexity: O(n)
  - **Insertion**: Time complexity: O(log n) on average, O(n) in the worst case
  - **Deletion**: Time complexity: O(log n) on average, O(n) in the worst case
- **Binary Search Tree (BST)**: A binary tree where the value of each node is greater than or equal to the values in all the nodes in that node's left subtree, and less than the values in all the nodes in that node's right subtree.
  - **Search**: Time complexity: O(log n) on average, O(n) in the worst case
  - **Insertion**: Time complexity: O(log n) on average, O(n) in the worst case
  - **Deletion**: Time complexity: O(log n) on average, O(n) in the worst case
- **AVL Tree**: A self-balancing binary search tree.
  - **Search/Insertion/Deletion**: Time complexity: O(log n)

Trees have applications in hierarchical data representation, file systems, and more.

### Graph
A graph is a non-linear data structure that consists of a finite set of nodes (or vertices) and a set of edges that connect these nodes. Some common graph types are:

- **Undirected Graph**: Edges have no orientation.
- **Directed Graph**: Edges have a specific direction.
- **Weighted Graph**: Edges have associated weights or costs.

The main operations on graphs are:

- **Traversal**: Depth-First Search (DFS) and Breadth-First Search (BFS)
  - DFS: Time complexity: O(|V| + |E|)
  - BFS: Time complexity: O(|V| + |E|)
- **Shortest Path**: Dijkstra's algorithm, Bellman-Ford algorithm
  - Dijkstra's: Time complexity: O((|V| + |E|) log |V|)
  - Bellman-Ford: Time complexity: O(|V||E|)
- **Minimum Spanning Tree**: Kruskal's algorithm, Prim's algorithm
  - Kruskal's: Time complexity: O(|E| log |V|)
  - Prim's: Time complexity: O((|V| + |E|) log |V|)

Graphs have applications in social networks, transportation networks, and more.

The time and space complexities provided are general guidelines, and the actual performance may vary depending on the specific implementation and the input data.
