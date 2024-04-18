1. Output of the program:
   ```c
   #include <stdio.h>
   void main() {
       int a = 40;
       float b;
       b = ++a;
       printf("%d, %f ", a, ++b);
   }
   ```
   (A) 41, 42.000000

2. Output of the program:
   ```c
   #include <stdio.h>
   void main() {
       int a = -7;
       float b;
       b = a++;
       printf("%d, %f ", a, ++b);
   }
   ```
   (A) -6, -7.000000

3. Output of the program:
   ```c
   #include <stdio.h>
   void main() {
       int i = -1;
       printf("sizeof(i) = %d", sizeof(i));
   }
   ```
   (D) sizeof(i) = 4

4. Output of the program:
   ```c
   #include <stdio.h>
   void main() {
       int x = -1, y = 1, z = 0;
       if (x && y++ && z)
           ++x, y++, --z;
       printf("%d, %d, %d", x++, y++, z++);
   }
   ```
   (C) -1, 2, 0

5. Output of the program:
   ```c
   #include <stdio.h>
   enum colors { RED, BROWN, ORANGE };
   void main() {
       printf("%ld..%f..%d", RED, BROWN, ORANGE);
   }
   ```
   (C) 0..1.000000..2

6. Output of the program:
   ```c
   #include <stdio.h>
   void main() {
       char M = 'M';
       printf("%d, %c", M, M);
   }
   ```
   (C) 76, M

7. Output of the program:
   ```c
   #include <stdio.h>
   void main() {
       int i = -9;
       printf("%d %d %d", i++, ++i, ++i);
   }
   ```
   (C) -7 -7 -8

8. Output of the program:
   ```c
   #include<stdio.h>
   void main() {
       int **ptr;
       int temp = 65;
       ptr[0] = &temp;
       printf("%d", ptr[0][0]);
   }
   ```
   (A) Compiler error (no memory allocated for `ptr`)

9. Output of the program:
   ```c
   #include <stdio.h>
   #include <stdlib.h>
   void main() {
       int *ptr;
       ptr = (int*)calloc(3, sizeof(int));
       ptr[2] = 30;
       printf("%d", *ptr);
       free(ptr);
   }
   ```
   (B) 0

10. Interrupt due to power failure is:
    (C) Hardware

11. Address of the next instruction to be executed is specified by:
    (D) PC

12. Auxiliary memory is also known as:
    (B) Secondary memory

13. BIOS means:
    (A) basic input/output system

14. Most appropriate scheduling in case of a time-shared operating system is:
    (B) RR (Round Robin)

15. If only one process can be able to access a particular resource at a time, then it is known as:
    (B) Mutual exclusion

16. Resource allocation graph is used to represent:
    (A) deadlock

17. Banker’s algorithm for resource allocation deals with:
    (D) deadlock avoidance

18. Page fault means:
    (B) required page is not available in main memory

19. Technique to move a process from main memory to secondary memory is:
    (D) Swapping

20. Demand paging is considered as:
    (C) fetching a page only when needed

21. Thrashing means a condition having:
    (D) excessive paging

22. Resulting value of the semaphore after operations is:
    (B) 13

23. fork( ) means:
    (B) Creation of new task

24. In file management, FAT means:
    (D) File Allocation Table

25. Output of the C++ program is:
    (A) 55;46.8

26. Output of the C++ program is:
    (A) Equal

27. Output of the C++ program is:
    (B) 0 1 2 3 4 5 6 7 8 9

28. Output of the C++ program is:
    (A) 100

29. Output of the C++ program is:
    (A) c1= 50, c2= 50; c1= 10, c2= 50

30. Output of the C++ program is:
    (A) 6

31. Output of the C++ program is:
    (A) Compile Error

32. Output of the C++ program is:
    (C) 2

33. Command used to create a new directory in shell script is:
    (D) mkdir

34. Command used to copy a file in shell script is:
    (C) cp

35. Command used to delete a file in shell script is:
    (D) rm

36. Command used to find out the difference between two files in Unix/Linux platform is:
    (A) diff

37. Command used to create a symbolic link in Unix/Linux platform is:
    (D) ln -s

38. Command used to view the inode number of a file in Unix/Linux platform is:
    (A) ls -i

39. Command used to specify the access mode for files in Unix/Linux platform is:
    (A) chmod

40. Command used to show current running processes in Unix/Linux platform is:
    (A) ps

41. Time complexity for insertion at a particular node in singly linked list is:
    (C) O(n)

42. Operation not permitted in stack data structure is:
    (D) Enqueue

43. In-degree of root node in tree data structure is always:
    (A) 0

44. Preorder traversal means:
    (A) Root → Left-Subtree → Right-Subtree

45. Wrong statement based on the characteristics of AVL tree data structure is:
    (D) AVL tree has O(n) search time complexity considering ‘n’ as number of nodes.

46. Example of non-linear data structure is:
    (B) Graph

47. Bubble sort algorithm has a worst-case time complexity of:
    (B) O(n^2)

48. Insertion sort algorithm has a best-case time complexity of:
    (A) O(n)

49. VC means:
    (A) Vapnik–Chervonenkis

50. Artificial Neural networks are:
    (A) computational

51. One-class SVM is:
    (A) unsupervised

52. Time complexity of K-Means clustering is:
    (B) O(kN^2)

53. Algorithm used

 to find out the shortest path between two points in a connected weighted graph is:
    (A) Kruskal

54. Forward–backward algorithm is used in case of HMM to compute:
    (A) posterior marginal

55. HMM is a specific instance of CRF which is known as:
    (A) conditional random fields

56. In FP-Growth Algorithm, FP means:
    (A) frequent pattern

57. Full form for PERT chart is:
    (C) Program Evaluation and Review Technique

58. Testing performed by development team is known as:
    (B) α testing

59. Prototyping model can be used when:
    (A) Technical solutions are unclear to the development team

60. Phase comes before the design phase in classical waterfall model is:
    (D) Requirements analysis and specification

61. Type of cohesion that is not mentioned is:
    (A) Projection

62. Type of coupling that is not mentioned is:
    (D) Stamp

63. Activities of the first quadrant of Spiral model are:
    (A) Determine objectives, alternatives and constraints

64. Black-box testing technique is:
    (D) Acceptance testing

65. Size of the header in User Datagram packet format is:
    (C) 4 bytes

66. Transmission Control Protocol (TCP) offers:
    (A) full-duplex

67. Example of a two-layer switch is:
    (A) bridge

68. A static routing table contains information:
    (A) entered manually

69. BOOTP is:
    (C) network layer protocol

70. ICMP always reports error messages to the original:
    (A) source

71. Program uses ICMP messages and TTL field in IP packet to find route is:
    (A) traceroute

72. SNMP is:
    (A) application level protocol

73. Key that can be derived directly from a Super Key is:
    (A) Primary key

74. Relational Algebra is:
    (A) Non-procedural

75. In case of union compatibility:
    (A) two relations must have same set of attributes.

76. Option not used with “ALTER table” command in SQL is:
    (B) Drop

77. Third normal form (3NF) removes ______________ from a relation:
    (C) Transitive dependency

78. Step not involved in query processing is:
    (D) Meta data organizer

79. Transaction state that does not exist is:
    (D) Updated

80. Normal form that does not have any partial functional dependencies is:
    (A) BCNF

81. Valid file operations in C programming are:
    (A) fopen, (B) fclose, (C) fprintf, (D) fscanf

82. Functions mentioned in “string.h” header file are:
    (A) strcat, (B) strcmp, (C) strlen

83. Basic elements of a computer are:
    (A) Central Processing Unit, (C) Main Memory

84. Correct I/O communication techniques are:
    (A) Direct Memory Access, (D) Interrupt Driven I/O

85. Correct buffering types in I/O management are:
    (A) Single buffering, (C) Double buffering

86. Correct disk scheduling algorithms are:
    (B) SSTF, (C) SCAN

87. Correct loop classifications are:
    (A) while loop is known as entry-controlled loop, (D) do-while loop is known as exit-controlled loop

88. Correct bitwise operators are:
    (C) & (bitwise AND), (D) | (bitwise OR)

89. Correct UNIX wildcard characters are:
    (A) *, (B) ?, (C) [ ], (D) { }

90. Command to show the list of files in shell script is:
    (A) ls, (B) ls -l

91. Correct Linked list types are:
    (A) Linear linked list, (B) Circular linked list, (C) Doubly linked list

92. Correct Linked list operations are:
    (A) Insertion of a node, (B) Deletion of a node, (C) Search a node

93. Correct learning types are:
    (A) Supervised, (B) Unsupervised, (C) Reinforcement

94. Authors of Apriori algorithm are:
    (A) Agrawal, (B) Srikant

95. Activities undertaken during maintenance in SDLC are:
    (A) Corrective maintenance, (B) Perfective maintenance

96. Properties of a good Software Requirement Specification (SRS) include:
    (A) Correctness, (B) Completeness, (C) Consistency

97. User Datagram Protocol (UDP) is a:
    (B) unreliable, (C) connectionless

98. Congestion in a network occurs because:
    (A) routers, (B) switches

99. Levels of Data Abstraction in architecture for Database system include:
    (A) View level, (B) Logical level, (C) Schema level

100. Examples of multi-valued attributes include:
    (A) Address, (B) Email ID
