# Operating System (OS)

## 1. Process
### Definition
A **Process** is a program in execution.

### States of a Process
- **New**: Process is being created.
- **Ready**: Process is waiting to be assigned to a CPU.
- **Running**: Process instructions are being executed.
- **Waiting**: Process is waiting for some event to occur.
- **Terminated**: Process has finished execution.

### Process Control Block (PCB)
A data structure used by the operating system to store all the information about a process.
- **Process ID (PID)**
- **Program Counter**
- **CPU Registers**
- **Memory Management Information**
- **I/O Status Information**

### Example
```plaintext
PCB {
  PID: 1234,
  State: Running,
  Program Counter: 3456,
  Registers: {...},
  ...
}
```

---

## 2. Thread
### Definition
A **Thread** is the smallest unit of processing that can be performed in an OS.

### Types of Threads
- **User Threads**: Managed by user-level libraries.
- **Kernel Threads**: Managed by the OS kernel.

### Multithreading Models
- **Many-to-One**: Many user threads mapped to one kernel thread.
- **One-to-One**: Each user thread mapped to a kernel thread.
- **Many-to-Many**: Many user threads mapped to many kernel threads.

### Example
```plaintext
Thread {
  TID: 1,
  State: Running,
  Program Counter: 2345,
  Registers: {...},
  ...
}
```

---

## 3. CPU Scheduling
### Definition
**CPU Scheduling** is the process of determining which process will own the CPU for execution while another process is on hold.

### Scheduling Algorithms
- **First-Come, First-Served (FCFS)**: Processes are scheduled in the order they arrive.
- **Shortest Job Next (SJN)**: Process with the smallest execution time is selected.
- **Round Robin (RR)**: Each process gets an equal share of the CPU time.
- **Priority Scheduling**: Process with the highest priority is selected.
- **Multilevel Queue Scheduling**: Processes are divided into different queues based on their priority.

### Example
```plaintext
Process Queue: [P1, P2, P3, P4]
```

---

## 4. Deadlock
### Definition
A **Deadlock** is a situation where a set of processes are blocked because each process is holding a resource and waiting for another resource held by another process.

### Necessary Conditions
- **Mutual Exclusion**: At least one resource must be held in a non-sharable mode.
- **Hold and Wait**: A process is holding at least one resource and waiting for additional resources.
- **No Preemption**: Resources cannot be forcibly taken from processes.
- **Circular Wait**: A set of processes are waiting for each other in a circular chain.

### Deadlock Handling
- **Deadlock Prevention**: Ensure that at least one of the necessary conditions cannot hold.
- **Deadlock Avoidance**: Use algorithms like Banker’s algorithm to avoid deadlocks.
- **Deadlock Detection**: Allow the system to enter a deadlock state and then recover.
- **Deadlock Recovery**: Recover from deadlock by terminating processes or preempting resources.

### Example
```plaintext
P1: Holds R1, waiting for R2
P2: Holds R2, waiting for R1
```

---

## 5. Synchronization
### Definition
**Synchronization** is the coordination of concurrent processes to ensure correct execution.

### Critical Section Problem
A **Critical Section** is a segment of code where shared resources are accessed.

### Solutions
- **Mutex Locks**: Ensures that only one process can enter the critical section at a time.
- **Semaphores**: Signaling mechanism to control access to the critical section.
- **Monitors**: High-level synchronization construct that controls access to shared data.

### Example
```c
// Semaphore Example
semaphore mutex = 1;

wait(mutex);
  // Critical Section
signal(mutex);
```

---

## 6. Memory Management
### Definition
**Memory Management** is the functionality of an operating system which handles or manages primary memory.

### Techniques
- **Paging**: Divides memory into fixed-size pages.
- **Segmentation**: Divides memory into variable-size segments.
- **Virtual Memory**: Uses hardware and software to allow a computer to compensate for physical memory shortages by temporarily transferring data from random access memory to disk storage.

### Example
```plaintext
Physical Memory: [Frame 0, Frame 1, Frame 2, ...]
Virtual Memory: [Page 0, Page 1, Page 2, ...]
```

---

## 7. Disk Management
### Definition
**Disk Management** involves managing disk storage resources efficiently.

### Disk Scheduling Algorithms
- **First-Come, First-Served (FCFS)**
- **Shortest Seek Time First (SSTF)**
- **SCAN (Elevator Algorithm)**
- **C-SCAN (Circular SCAN)**
- **LOOK and C-LOOK**

### Example
```plaintext
Disk Queue: [98, 183, 37, 122, 14, 124, 65, 67]
```

---

## 8. File Management
### Definition
**File Management** refers to the way the operating system handles files, including their creation, deletion, reading, writing, and access control.

### File System Structure
- **File**: Basic unit of storage.
- **Directory**: Contains information about files.
- **Path**: Specifies a unique location in the file system.

### File Access Methods
- **Sequential Access**: Read/write sequentially.
- **Direct Access**: Read/write in arbitrary order.
- **Indexed Access**: Use an index to access files.

### Example
```plaintext
Root Directory
  |
  +-- home
  |   |
  |   +-- user
  |       |
  |       +-- file.txt
  |
  +-- etc
      |
      +-- config.conf
```
