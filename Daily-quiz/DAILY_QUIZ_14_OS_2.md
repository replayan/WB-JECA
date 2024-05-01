# Operating System QUIZ

Date: May 01, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

---

1. **Which process can be affected by other processes executing in the system?**

- [ ] child process
- [ ] parent process
- [ ] init process
- [x] cooperating process

**Explanation:**
A cooperating process is a process that shares resources or data with other processes. It can be affected by the actions of other processes, such as resource contention, data corruption, or synchronization issues. Child and parent processes are related through process creation, while the init process is the first process that runs when the system boots up.

2. **Thread synchronization is required because \_\_\_\_\_\_\_\_\_\_\_**

- [ ] all threads of a process share the same address space
- [ ] all threads of a process share the same global variables
- [ ] all threads of a process can share the same files
- [x] all of the mentioned

**Explanation:**
Thread synchronization is necessary because all threads within the same process share the same address space, including data, code, and resources. Without proper synchronization, multiple threads accessing shared data or resources simultaneously can lead to race conditions, data corruption, and other concurrency issues. Sharing global variables and files alone does not necessitate synchronization if the threads do not access them concurrently.

3. **The LRU (Least Recently Used) algorithm**

- [ ] pages out pages that have been used recently
- [ ] pages out pages that have not been used recently
- [x] pages out pages that have been least used recently
- [ ] pages out the first page in a given area

**Explanation:**
The LRU (Least Recently Used) algorithm is a page replacement algorithm that pages out (removes) the page that has not been used or accessed for the longest time. It keeps track of the most recently used pages and replaces the page that has not been accessed for the longest duration when a new page needs to be loaded into memory.

4. **A process can be terminated due to ...**

- [ ] normal exit
- [ ] fatal error
- [ ] killed by another process
- [x] all of the mentioned

**Explanation:**
A process can be terminated due to various reasons, including:
1. Normal exit: When the process completes its execution successfully.
2. Fatal error: When the process encounters an unrecoverable error, such as a segmentation fault or an invalid instruction.
3. Killed by another process: When another process with appropriate permissions sends a termination signal to the process.

---

5. **3 page frames have been allocated to a process. Here, we assume that none of the process's pages is available initially in the memory, and the process creates this sequence of page references: 1, 2, 1, 3, 7, 4, 5, 6, 3, 1 (reference string). If an optimal page replacement policy is utilized, then how many page faults would occur for the reference string mentioned above?**

- [ ] 10
- [ ] 9
- [ ] 8
- [x] 7

**Explanation:**
With an optimal page replacement policy (like the Least Recently Used algorithm), the number of page faults for the given reference string would be 7.

Initially, the page frames are empty.
Reference 1: Page fault, page 1 is loaded.
Reference 2: Page fault, page 2 is loaded.
Reference 1: No page fault.
Reference 3: Page fault, page 3 is loaded, and page 1 is replaced (since it was least recently used).
Reference 7: Page fault, page 7 is loaded, and page 2 is replaced (since it was least recently used).
Reference 4: Page fault, page 4 is loaded, and page 3 is replaced (since it was least recently used).
Reference 5: Page fault, page 5 is loaded, and page 7 is replaced (since it was least recently used).
Reference 6: Page fault, page 6 is loaded, and page 4 is replaced (since it was least recently used).
Reference 3: No page fault.
Reference 1: No page fault.

So, the total number of page faults is 7.
