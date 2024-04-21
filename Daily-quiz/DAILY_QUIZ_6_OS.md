# Operating Systems Quiz

## Question 1:
**Scheduling is done so as to ____________**

- [ ] increase the turnaround time
- [x] decrease the turnaround time
- [ ] keep the turnaround time same
- [ ] there is no relation between scheduling and turnaround time

*Explanation:* Scheduling is done to decrease the turnaround time. By efficiently organizing tasks, resources, and processes, scheduling aims to minimize the time it takes to complete a task or project, thus reducing the turnaround time.

## Question 2:
**To avoid the race condition, the number of processes that may be simultaneously inside their critical section is ____________**

- [ ] 8
- [x] 1
- [ ] 16
- [ ] 0

*Explanation:* To avoid a race condition, typically only one process is allowed to be inside its critical section at a time. This ensures that the integrity of shared resources is maintained and prevents conflicts that can occur when multiple processes attempt to access the same resource simultaneously.

## Question 3:
**A disk scheduling algorithm in an operating system causes the disk arm to move back and forth across the disk surface in order to service all requests in its path. This is a ____________**

- [ ] First come first served
- [ ] Shortest Seek Time First (SSTE)
- [x] Scan
- [ ] FIFO

*Explanation:* The disk scheduling algorithm described, where the disk arm moves back and forth across the disk surface to service all requests in its path, is known as Scan. This algorithm is also sometimes referred to as the elevator algorithm because the movement of the disk arm resembles that of an elevator moving up and down a building.

## Question 4:
**What is virtual memory?**

- [ ] A type of computer storage that is slower than main memory
- [ ] A type of computer memory that is used to temporarily store data that is being actively used
- [x] A technique used by operating systems to allow a computer to use more memory than it physically has
- [ ] A type of memory that is used for long-term storage of data and files

*Explanation:* Virtual memory is a technique used by operating systems to allow a computer to use more memory than it physically has. It utilizes a combination of hardware and software to create an illusion for processes that they have more memory than is actually available. This illusion is achieved by transferring data between the RAM and the hard disk when the RAM becomes full, allowing the system to handle larger programs or multiple programs simultaneously.

## Question 5:
**The circular wait condition can be prevented by ____________**

- [x] defining a linear ordering of resource types
- [ ] using thread
- [ ] using pipes
- [ ] all of the mentioned

*Explanation:* The circular wait condition in resource allocation can be prevented by defining a linear ordering of resource types. This means establishing a hierarchy or precedence among the resource types, ensuring that each process requests resources in a specific order and releases them in the reverse order. By enforcing this ordering, circular waits are avoided, as processes can only request resources that are lower in the hierarchy than the ones they already hold.
