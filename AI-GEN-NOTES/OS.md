### Process

- **Definition**: A process is a program in execution. It is a unit of work that is executed by the operating system.
- **Characteristics**:
  - **Program Counter (PC)**: The current instruction being executed.
  - **Registers**: Small amount of memory that stores data temporarily.
  - **Stack**: A region of memory that stores data temporarily.
  - **Open Files**: Files that are currently being used by the process.
- **Process States**:
  - **Newborn**: The process is being created.
  - **Running**: The process is currently being executed.
  - **Waiting**: The process is waiting for some event to occur.
  - **Zombie**: The process has finished execution but its parent process has not yet acknowledged it.
  - **Dead**: The process has finished execution and its parent process has acknowledged it.
- **Process Creation**:
  - **Fork**: Creates a new process by duplicating an existing process.
  - **Exec**: Loads a new program into memory and starts executing it.
- **Process Termination**:
  - **Exit**: The process terminates normally.
  - **Kill**: The process is terminated by the operating system.

### Thread

- **Definition**: A thread is a lightweight process that shares the same memory space as other threads within the same process.
- **Characteristics**:
  - **Program Counter (PC)**: The current instruction being executed.
  - **Registers**: Small amount of memory that stores data temporarily.
  - **Stack**: A region of memory that stores data temporarily.
- **Thread States**:
  - **Running**: The thread is currently being executed.
  - **Waiting**: The thread is waiting for some event to occur.
  - **Sleeping**: The thread is waiting for a specific amount of time to pass.
  - **Zombie**: The thread has finished execution but its parent thread has not yet acknowledged it.
  - **Dead**: The thread has finished execution and its parent thread has acknowledged it.
- **Thread Creation**:
  - **Create**: Creates a new thread within a process.
- **Thread Termination**:
  - **Exit**: The thread terminates normally.
  - **Kill**: The thread is terminated by the operating system.

### CPU Scheduling

- **Definition**: CPU scheduling is the process of allocating the CPU to different processes.
- **Types**:
  - **Preemptive Scheduling**: The operating system can interrupt a process at any time to schedule another process.
  - **Non-Preemptive Scheduling**: The operating system cannot interrupt a process once it has been allocated the CPU.
- **Scheduling Algorithms**:
  - **Preemptive Scheduling**:
    - **Round Robin (RR)**: Each process is given a fixed time slice (called a time quantum) to execute before the operating system switches to the next process.
    - **Shortest Job First (SJF)**: The process with the shortest burst time is executed first.
    - **Priority Scheduling**: The process with the highest priority is executed first.
  - **Non-Preemptive Scheduling**:
    - **First Come First Serve (FCFS)**: The process that arrives first is executed first.
    - **Shortest Job First (SJF)**: The process with the shortest burst time is executed first.
    - **Priority Scheduling**: The process with the highest priority is executed first.
- **CPU Scheduling Advantages and Disadvantages**:
  - **Preemptive Scheduling**:
    - **Advantages**:
      - **Improved CPU Utilization**: The CPU is utilized more efficiently as processes are switched quickly.
      - **Improved Response Time**: The response time is improved as processes are executed quickly.
    - **Disadvantages**:
      - **Overheads**: There are overheads associated with context switching and interrupt handling.
      - **Starvation**: A process with a high priority may starve if a process with a lower priority is executed for a long time.
  - **Non-Preemptive Scheduling**:
    - **Advantages**:
      - **Low Overheads**: There are low overheads associated with context switching and interrupt handling.
      - **No Starvation**: A process with a high priority will not starve as it will be executed immediately.
    - **Disadvantages**:
      - **Poor CPU Utilization**: The CPU is utilized poorly as processes are executed sequentially.
      - **Long Response Time**: The response time is long as processes are executed sequentially.

### Deadlock

- **Definition**: Deadlock is a situation where two or more processes are blocked indefinitely, each waiting for the other to release a resource.
- **Causes**:
  - **Mutual Exclusion**: Two or more processes are competing for the same resource.
  - **Hold and Wait**: A process is holding a resource and waiting for another resource.
  - **No Preemption**: The operating system cannot interrupt a process once it has been allocated a resource.
  - **Circular Wait**: A process is waiting for a resource that is held by another process, which is waiting for a resource held by the first process.
- **Detection**:
  - **Resource Type**: The type of resource that is causing the deadlock.
  - **Process ID**: The ID of the process that is causing the deadlock.
- **Prevention**:
  - **Avoid Mutual Exclusion**: Ensure that processes do not compete for the same resource.
  - **Avoid Hold and Wait**: Ensure that processes do not hold a resource and wait for another resource.
  - **Prevent No Preemption**: Ensure that the operating system can interrupt a process once it has been allocated a resource.
  - **Prevent Circular Wait**: Ensure that processes do not wait for a resource that is held by another process.

### Synchronization

- **Definition**: Synchronization is the process of controlling access to shared resources by multiple processes.
- **Types**:
  - **Mutual Exclusion**: Ensuring that only one process can access a shared resource at a time.
  - **Synchronization**: Ensuring that multiple processes access shared resources in a coordinated manner.
- **Synchronization Techniques**:
  - **Semaphores**: A variable that can be used to control access to a shared resource.
  - **Monitors**: A synchronization primitive that allows processes to communicate with each other.
  - **Locks**: A synchronization primitive that allows processes to access a shared resource.

### Memory Management

- **Definition**: Memory management is the process of managing the memory used by processes.
- **Types**:
  - **Contiguous Allocation**: Allocating memory in a contiguous block.
  - **Non-Contiguous Allocation**: Allocating memory in non-contiguous blocks.
- **Memory Allocation**:
  - **Dynamic Memory Allocation**: Allocating memory at runtime.
  - **Static Memory Allocation**: Allocating memory at compile time.
- **Memory Protection**:
  - **Segmentation**: Dividing memory into segments and protecting each segment.
  - **Paging**: Dividing memory into pages and protecting each page.
- **Virtual Memory**:
  - **Definition**: Virtual memory is a memory management technique that provides an "idealized abstraction of the storage resources that are actually available on a given machine".
  - **Properties**:
    - **Memory Virtualization**: Virtual memory makes application programming easier by hiding fragmentation of physical memory.
    - **Address Translation**: The operating system maps memory addresses used by a program into physical addresses in computer memory.
    - **Paging**: The operating system divides memory into pages and maps virtual addresses into physical addresses.
    - **Segmentation**: The operating system divides memory into segments and maps virtual addresses into physical addresses.

### Disk Management

- **Definition**: Disk management is the process of organizing and maintaining the storage on a computer's hard disk.
- **Tasks**:
  - **Partitioning**: Dividing the hard disk into separate areas, each of which is called a partition.
  - **Formatting**: Formatting the partitions to different file systems.
  - **Defragmentation**: Defragmenting the disk to improve disk performance.
  - **Backup**: Backing up the disk to ensure data safety.
- **Disk Management Tools**:
  - **Disk Management Tool**: A tool that can be used to manage disk partitions and formatting.
  - **Disk Defragmenter Tool**: A tool that can be used to defragment the disk.

### File Management

- **Definition**: File management is the process of managing files used by processes.
- **Types**:
  - **File Allocation**: Allocating space on the disk for files.
  - **File Protection**: Protecting files from unauthorized access.
- **File Operations**:
  - **Create**: Creating a new file.
  - **Read**: Reading data from a file.
  - **Write**: Writing data to a file.
  - **Delete**: Deleting a file.
- **File Systems**:
  - **File Allocation Table (FAT)**: A file system that uses a table to manage file allocation.
  - **Inode**: A file system that uses an inode to manage file allocation.
  - **Journaling File System**: A file system that uses a journal to manage file allocation.

### Conclusion

- **Summary**: Operating systems manage processes, threads, CPU scheduling, deadlock, synchronization, memory management, disk management, and file management.
- **Key Points**:
  - **Process**: A process is a program in execution.
  - **Thread**: A thread is a lightweight process that shares the same memory space as other threads within the same process.
  - **CPU Scheduling**: CPU scheduling is the process of allocating the CPU to different processes.
  - **Deadlock**: Deadlock is a situation where two or more processes are blocked indefinitely, each waiting for the other to release a resource.
  - **Synchronization**: Synchronization is the process of controlling access to shared resources by multiple processes.
  - **Memory Management**: Memory management is the process of managing the memory used by processes.
  - **Disk Management**: Disk management is the process of organizing and maintaining the storage on a computer's hard disk.
  - **File Management**: File management is the process of managing files used by processes.

# SOURCE:

[1] https://www.geeksforgeeks.org/preemptive-and-non-preemptive-scheduling/

[2] https://www.tutorialspoint.com/disk-management-in-operating-system

[3] https://en.wikipedia.org/wiki/Virtual_memory

[4] https://testbook.com/key-differences/difference-between-preemptive-and-non-preemptive-scheduling

[5] https://www.geeksforgeeks.org/difference-between-preemptive-and-non-preemptive-cpu-scheduling-algorithms/

[6] https://www.guru99.com/preemptive-vs-non-preemptive-scheduling.html

[7] https://www.javatpoint.com/preemptive-vs-non-preemptive-scheduling

[8] https://study.com/academy/lesson/preemptive-vs-non-preemptive-process-scheduling.html

[9] https://www.turing.com/kb/different-types-of-non-preemptive-cpu-scheduling-algorithms

[10] https://www.geeksforgeeks.org/disk-management-in-operating-system/

[11] https://www.spiceworks.com/tech/devops/articles/what-is-virtual-memory/

[12] https://byjus.com/gate/difference-between-preemptive-and-non-preemptive-scheduling/

[13] https://www.geeksforgeeks.org/virtual-memory-in-operating-system/

[14] https://dzone.com/articles/deadlock-free-synchronization-in-java

[15] https://www.techtarget.com/searchstorage/definition/virtual-memory

[16] https://www.geeksforgeeks.org/thread-in-operating-system/

[17] https://www.javatpoint.com/disk-management-in-operating-system

[18] https://learn.microsoft.com/en-us/windows-server/storage/disk-management/overview-of-disk-management

[19] https://www.scaler.com/topics/operating-system/disk-management/

[20] https://www.javatpoint.com/os-virtual-memory
