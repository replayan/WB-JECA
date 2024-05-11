# Operating System QUIZ

Date: May 11, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

---

## Multiple Choice Questions:

1. **To avoid the race condition, the number of processes that may be simultaneously inside their critical section is:**
   - **Options:**
     A) 8
     B) 1
     C) 16
     D) 0
   - **Correct Answer:** B) 1
   - **Explanation:** To avoid race conditions, typically only one process should be allowed inside its critical section at a time. This ensures that shared resources are not accessed concurrently, preventing data corruption or inconsistencies.

2. **Which of the following is CORRECT?**
   - **Options:**
     A) The page fault rate always increases with the increase in the number of frames.
     B) The page fault is independent of the number of frames.
     C) The page fault rate is inversely proportional to the degree of multiprogramming.
     D) The page fault rate sometimes increases with the increase in the number of frames for few page replacement policies.
   - **Correct Answer:** D) The page fault rate sometimes increases with the increase in the number of frames for few page replacement policies.
   - **Explanation:** While increasing the number of frames can often reduce the page fault rate by allowing more pages to be kept in memory, certain page replacement policies (such as Belady's Optimal Algorithm) can exhibit anomalous behavior where increasing the number of frames may paradoxically lead to an increase in the page fault rate.

3. **The circular wait condition can be prevented by:**
   - **Options:**
     A) Defining a linear ordering of resource types.
     B) Using threads.
     C) Using pipes.
     D) All of the mentioned.
   - **Correct Answer:** A) Defining a linear ordering of resource types.
   - **Explanation:** Defining a linear ordering of resource types ensures that processes always request resources in the same order, breaking the circular dependency that leads to deadlock.

4. **_______ is the most appropriate scheduling in case of a time-shared operating system.**
   - **Options:**
     A) FCFS
     B) RR
     C) SJF
     D) SRTF
   - **Correct Answer:** B) RR (Round Robin)
   - **Explanation:** In a time-shared operating system, where multiple processes are competing for CPU time, Round Robin scheduling is often the most appropriate choice. It ensures fairness by giving each process a small unit of CPU time (a time slice or quantum) and then moving on to the next process in the queue.

5. **The number of processes completed per unit time is known as:**
   - **Options:**
     A) Output
     B) Throughput
     C) Efficiency
     D) Capacity
   - **Correct Answer:** B) Throughput
   - **Explanation:** Throughput is a measure of the efficiency of a system in terms of the amount of work done within a given period of time. It represents the number of processes completed per unit time and is a key performance metric in system evaluation.
