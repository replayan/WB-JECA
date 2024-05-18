# Data Structures

## 1. Searching
### Linear Search
Searches each element in the list sequentially until the desired element is found.
- **Time Complexity**: O(n)
- **Space Complexity**: O(1)

### Binary Search
Searches a sorted list by repeatedly dividing the search interval in half.
- **Time Complexity**: O(log n)
- **Space Complexity**: O(1)
- **Requirement**: The array must be sorted.

### Example
```python
# Binary Search Example in Python
def binary_search(arr, target):
    low, high = 0, len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    return -1
```

---

## 2. Sorting
### Bubble Sort
Repeatedly swaps adjacent elements if they are in the wrong order.
- **Time Complexity**: O(n^2)
- **Space Complexity**: O(1)

### Selection Sort
Selects the smallest element from an unsorted list and swaps it with the first unsorted element.
- **Time Complexity**: O(n^2)
- **Space Complexity**: O(1)

### Insertion Sort
Builds the final sorted array one item at a time.
- **Time Complexity**: O(n^2)
- **Space Complexity**: O(1)

### Merge Sort
Divides the array into halves, sorts them, and merges them.
- **Time Complexity**: O(n log n)
- **Space Complexity**: O(n)

### Quick Sort
Divides the array into partitions and recursively sorts the partitions.
- **Time Complexity**: O(n log n) on average, O(n^2) in the worst case.
- **Space Complexity**: O(log n) on average, O(n) in the worst case.

Here's a table summarizing the time complexity (TC) and space complexity (SC) of common sorting algorithms in their best, average, and worst cases:

| Algorithm       | Best Case TC  | Average Case TC | Worst Case TC | Space Complexity (SC) |
|-----------------|---------------|-----------------|---------------|-----------------------|
| **Bubble Sort** | O(n)          | O(n²)           | O(n²)         | O(1)                  |
| **Insertion Sort** | O(n)      | O(n²)           | O(n²)         | O(1)                  |
| **Selection Sort** | O(n²)      | O(n²)           | O(n²)         | O(1)                  |
| **Merge Sort**  | O(n log n)    | O(n log n)      | O(n log n)    | O(n)                  |
| **Quick Sort**  | O(n log n)    | O(n log n)      | O(n²)         | O(log n) (average case), O(n) (worst case) |
| **Heap Sort**   | O(n log n)    | O(n log n)      | O(n log n)    | O(1)                  |
| **Counting Sort** | O(n + k)    | O(n + k)        | O(n + k)      | O(k)                  |
| **Radix Sort**  | O(nk)         | O(nk)           | O(nk)         | O(n + k)              |
| **Bucket Sort** | O(n + k)      | O(n + k)        | O(n²)         | O(n)                  |
| **Shell Sort**  | O(n log n)    | O(n^(3/2))      | O(n²)         | O(1)                  |
| **Tim Sort**    | O(n)          | O(n log n)      | O(n log n)    | O(n)                  |

- **n**: Number of elements to be sorted
- **k**: Range of the numbers in Counting Sort and Radix Sort
- **log n**: Logarithm base 2, though the base of the logarithm doesn't change the complexity class

Note : That some algorithms like Quick Sort have different worst-case and average-case space complexities depending on the implementation.

---

## 3. Stack
### Definition
A **Stack** is a linear data structure that follows the Last In First Out (LIFO) principle.

### Operations
- **Push**: Add an element to the top of the stack.
- **Pop**: Remove the top element from the stack.
- **Peek/Top**: Return the top element without removing it.
- **IsEmpty**: Check if the stack is empty.

### Time and Space Complexities
- **Push**: O(1)
- **Pop**: O(1)
- **Peek/Top**: O(1)
- **Space Complexity**: O(n) for n elements.

### Example
```python
# Stack Example in Python
class Stack:
    def __init__(self):
        self.items = []
        
    def push(self, item):
        self.items.append(item)
        
    def pop(self):
        if not self.is_empty():
            return self.items.pop()
        
    def peek(self):
        if not self.is_empty():
            return self.items[-1]
        
    def is_empty(self):
        return len(self.items) == 0
```

---

## 4. Queue
### Definition
A **Queue** is a linear data structure that follows the First In First Out (FIFO) principle.

### Operations
- **Enqueue**: Add an element to the end of the queue.
- **Dequeue**: Remove the front element from the queue.
- **Front**: Return the front element without removing it.
- **IsEmpty**: Check if the queue is empty.

### Time and Space Complexities
- **Enqueue**: O(1)
- **Dequeue**: O(1)
- **Front**: O(1)
- **Space Complexity**: O(n) for n elements.

### Example
```python
# Queue Example in Python
class Queue:
    def __init__(self):
        self.items = []
        
    def enqueue(self, item):
        self.items.append(item)
        
    def dequeue(self):
        if not self.is_empty():
            return self.items.pop(0)
        
    def front(self):
        if not self.is_empty():
            return self.items[0]
        
    def is_empty(self):
        return len(self.items) == 0
```

---

## 5. Linked List
### Definition
A **Linked List** is a linear data structure where each element is a separate object, called a node, which contains a data part and a reference (link) to the next node in the sequence.

### Types
- **Singly Linked List**: Each node points to the next node.
- **Doubly Linked List**: Each node points to both the next and the previous nodes.
- **Circular Linked List**: The last node points back to the first node.

### Operations
- **Insertion**: O(1) for inserting at the beginning, O(n) for inserting at the end.
- **Deletion**: O(1) for deleting from the beginning, O(n) for deleting from the end.
- **Traversal**: O(n)

### Example
```python
# Singly Linked List Example in Python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def insert_at_beginning(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node

    def insert_at_end(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        last_node = self.head
        while last_node.next:
            last_node = last_node.next
        last_node.next = new_node

    def delete_node(self, key):
        temp = self.head
        if temp and temp.data == key:
            self.head = temp.next
            temp = None
            return
        prev = None
        while temp and temp.data != key:
            prev = temp
            temp = temp.next
        if temp is None:
            return
        prev.next = temp.next
        temp = None

    def traverse(self):
        current = self.head
        while current:
            print(current.data, end=" -> ")
            current = current.next
        print("None")
```

---

## 6. Tree
### Definition
A **Tree** is a hierarchical data structure consisting of nodes, with a single root node and sub-nodes forming a parent-child relationship.

### Types
- **Binary Tree**: Each node has at most two children.
- **Binary Search Tree (BST)**: A binary tree where the left child has smaller value and the right child has larger value.
- **AVL Tree**: A self-balancing binary search tree.
- **Heap**: A special tree-based data structure that satisfies the heap property.

### Tree Traversals
- **Inorder (Left, Root, Right)**: O(n)
- **Preorder (Root, Left, Right)**: O(n)
- **Postorder (Left, Right, Root)**: O(n)

### Example
```python
# Binary Tree Traversal Example in Python
class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None

def inorder_traversal(root):
    if root:
        inorder_traversal(root.left)
        print(root.data, end=" ")
        inorder_traversal(root.right)

def preorder_traversal(root):
    if root:
        print(root.data, end=" ")
        preorder_traversal(root.left)
        preorder_traversal(root.right)

def postorder_traversal(root):
    if root:
        postorder_traversal(root.left)
        postorder_traversal(root.right)
        print(root.data, end=" ")
```

---

## 7. Graph
### Definition
A **Graph** is a collection of nodes (vertices) and edges connecting them.

### Types
- **Directed Graph (Digraph)**: Edges have a direction.
- **Undirected Graph**: Edges do not have a direction.
- **Weighted Graph**: Edges have weights (costs).

### Graph Representations
- **Adjacency Matrix**: A 2D array to represent edges.
- **Adjacency List**: A list of lists to represent edges.

### Graph Traversals
- **Depth-First Search (DFS)**
  - **Time Complexity**: O(V + E)
  - **Space Complexity**: O(V)
  
- **Breadth-First Search (BFS)**
  - **Time Complexity**: O(V + E)
  - **Space Complexity**: O(V)

### Example
```python
# Graph Representation and Traversal Example in Python
from collections import defaultdict, deque

class Graph:
    def __init__(self):
        self.graph = defaultdict(list)

    def add_edge(self, u, v):
        self.graph[u].append(v)

    def bfs(self, start):
        visited = set()
        queue = deque([start])
        visited.add(start)

        while

 queue:
            vertex = queue.popleft()
            print(vertex, end=" ")

            for neighbor in self.graph[vertex]:
                if neighbor not in visited:
                    queue.append(neighbor)
                    visited.add(neighbor)

    def dfs(self, start, visited=None):
        if visited is None:
            visited = set()
        visited.add(start)
        print(start, end=" ")

        for neighbor in self.graph[start]:
            if neighbor not in visited:
                self.dfs(neighbor, visited)
```
