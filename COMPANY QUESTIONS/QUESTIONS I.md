 Updating the character’s position.
 
Rendering the game graphics.

Detecting player input (e.g., swipes or taps).

Updating the score and game state.

 All these threads are managed entirely by the game, without involving the operating system's kernel.
 

If one thread encounters a blocking operation, such as a file read or a long calculation, the whole game could pause.

 If one thread is stuck, the entire process can get stuck because the OS can’t schedule other threads of the game independently.

 Kernel-Level Threads (KLTs) - Example: Web Server (Apache)

In a web server like Apache, the situation is more complex, as multiple user requests (e.g., visiting a webpage) are being processed simultaneously.

OS-Managed Multitasking: Each request, such as loading a webpage, is handled by its own thread. Unlike ULTs, these threads are managed by the operating system kernel, not the application itself. The kernel can schedule these threads across multiple CPU cores and handle them independently.

Handling Blocking Calls: When a thread needs to perform a blocking operation (e.g., waiting for a response from a database), the kernel knows to stop that thread temporarily but allows other threads to keep running. For instance:
    
Thread A is waiting for data from a database (blocking).

Thread B is still able to load and serve a different webpage without being affected by Thread A’s wait.

Concurrency and Performance: The OS allocates resources efficiently. For example, if you have a multi-core processor, the OS can run multiple threads in parallel across cores. Even if some threads are blocked, other threads continue running, maximizing system performance.

Analogy:

In this case, imagine a restaurant kitchen with multiple chefs (threads), and the head chef (OS kernel) manages them. If one chef is waiting for ingredients, the others can continue cooking, ensuring that the kitchen runs smoothly without delays.
Key Points of Understanding:
User-Level Threads (ULTs):

Faster Switching: Switching between threads in user space is faster since there’s no kernel involvement.
Single Block Affects All: If one thread encounters a blocking operation, the entire process can block because the OS treats the process as a whole.
Less Overhead: The process manages threads on its own, reducing overhead since there’s no need for system calls to the kernel for thread operations.

Kernel-Level Threads (KLTs):

Concurrency and Parallelism: Threads are managed independently by the kernel, allowing true parallelism on multi-core systems.
Non-blocking Execution: A blocking call on one thread doesn’t affect others, as the kernel can continue executing other threads.
Increased Overhead: Context switching between kernel threads is slower than ULTs because it involves the kernel and system calls.

 Privilege Level:

User Mode: Runs with low privileges. Applications (e.g., web browsers, games) cannot directly access hardware or system resources. This ensures that if something goes wrong, it won’t affect the entire system.
Kernel Mode: Runs with full privileges. The operating system kernel can access hardware (e.g., CPU, memory, I/O devices) and manage system-level tasks like memory management, process scheduling, and hardware control.

 User Mode: Crashes in user mode (e.g., a browser crash) affect only the specific application, not the entire system.

Kernel Mode: Errors in kernel mode (e.g., faulty drivers) can crash the entire system (e.g., blue screen on Windows).

 Web Browser (Network Request)

User Mode: A web browser wants to load a webpage. It needs to send a request over the network.

System Call (Mode Switch): The browser makes a system call to access the network hardware (e.g., through the send() system call). The CPU 

switches to kernel mode to manage network communication.
    
Back to User Mode: Once the data is sent, the CPU switches back to user mode, and the browser continues its execution, waiting for a response.

 Example: A web browser runs in user mode. It can render web pages but cannot directly access the network or files.

 Example: The operating system kernel handles a network request on behalf of the browser using system calls (e.g., send()).

 The MMU is sometimes housed in a separate Integrated Chip (IC), but it is typically found inside the central processing unit (CPU) of the 
 
 computer. The MMU receives all inputs for data requests and decides whether to retrieve the data from ROM or RAM storage.

Why do we need logical address?



The CPU uses logical address as a reference to get to the real physical memory location.

 What is paging?

What is main memory, and difference between main and secondary memory?

What is segmentation?

What is thrashing?
 Can cache memory be upgraded?
Cache memory is built into the CPU or located very close to it, so it cannot be upgraded separately like RAM. To get more or faster cache, you would need to upgrade the entire CPU

 How does cache memory work?
Cache memory works by storing copies of frequently accessed data from the main memory. When the CPU needs data, it first checks the cache. If the data is found (a “cache hit”), it is quickly accessed.

If not (a “cache miss”), the data is fetched from the slower main memory.

 What is mutex? What is spin lock? what is Critical Section? 
 
Given 2 resources and 4 threads. One thread locked the CS. How does other threads acquire the CS?

What are System Calls? Different types of system calls?

 Explain Paging
 
What is RAID?
    
What is process?

What is context switching? 
    
What are different types of scheduling algorithms?

Working of Round Robin Algorithm.

How Process is created? What is process table? What is PCB(Process Control Block)? 

What are different types of attributes in PCB?

How does OS perform context switching?

What happens when we press a keyboard key? Explained him the steps involved in hardware level, OS level, and CPU level.

What is system call?
    
What is User space and kernal space?

Explain the memory layout of process.
    
 What is a semaphore?

 
What is System calls and explain it’s working?

What is a Kernel and what are the types of Kernel available?

 https://www.youtube.com/live/X9rIXqHHhTg?si=rGrsNTnXr5F7pMx1


https://www.linkedin.com/posts/parasmayur_%F0%9D%90%8B%F0%9D%90%A2%F0%9D%90%A7%F0%9D%90%AE%F0%9D%90%B1-%F0%9D%90%82%F0%9D%90%A1%F0%9D%90%9E%F0%9D%90%9A%F0%9D%90%AD%F0%9D%90%AC%F0%9D%90%A1%F0%9D%90%9E%F0%9D%90%9E%F0%9D%90%AD-%F0%9D%90%85%F0%9D%90%A8%F0%9D%90%AB-%F0%9D%90%84-activity-7245719286688690176-lqIZ?utm_source=share&utm_medium=member_android

 What are the Different roles/components of OS?
 
What is Inter-Process Communication? Its Types.Explain

Scheduling Algorithms

Types of Memory

Hierarchy of Memory in Computers.

 what is the basic difference between process and thread.Why actually do we need thread and in what scenario will it be useful to use thread.

 If our system is multcore and I wrote a program.Will the program be run by threads on its own or user has to do something in code to utilize threads concept in multicore system?
 
Draw process state Diagram. Explain the scenarios/events in which the transitions from one state to other will occur. He asked it for all states.

Why do we need process synchronization and tell mechanisms to deal with it?

 What do you  know in OS.
4.   What is process, thread? Difference Between process and thread.

https://www.geeksforgeeks.org/operarting-system-thread/

5.   What resources does a process use?How does the process
6.   
   resources information is maintained?https://www.geeksforgeeks.org/operating-system-process-table-process-control-block-pcb/

7.   What resources do threads use?https://www.geeksforgeeks.org/operarting-system-thread/
   
9.   What should we do if we do not want to share a file among threads?

10.   What are locks?https://www.geeksforgeeks.org/lock-variable-synchronization-mechanism/
    
12.   What is mutex ?What is semaphore? Difference between them.
https://www.geeksforgeeks.org/mutex-vs-semaphore/

10.Mutex vs Binary semaphore? Are they logically equivalent ?https://stackoverflow.com/questions/62814/difference-between-binary-semaphore-and-mutex

11.What is virtual memory  and why do we use it?https://www.geeksforgeeks.org/virtual-memory-operating-systems/

12.What is demand paging? How to map logical to physical address?https://www.geeksforgeeks.org/virtual-memory-operating-systems/
13.Which address is known to CPU?

14.What  is volatile keyword? Why do we need it?https://www.geeksforgeeks.org/understanding-volatile-qualifier-c-set-1-introduction/https://www.geeksforgeeks.org/understanding-volatile-qualifier-in-c/

15.What is static variable ?Show by example.https://www.geeksforgeeks.org/static-variables-in-c/
16.Where does static variable get stored?https://www.geeksforgeeks.org/memory-layout-of-c-program/
 What is segmentation fault?

Problem approach
Segmentation fault is a specific kind of error caused by accessing memory that “does not belong to you.” 

When a piece of code tries to do read and write operation in a read only location in memory or freed block of memory, it is known as core 

dump. It is an error indicating memory corruption


 What is kernel?
 
-What is system calls, how they are executed?

-Questions based on process synchronization, mutex, semaphores (binary and counting)
-Linux file system, inode

-Virtual memory, addressing, paging, segmentation, fragmentation

-Page fault, thrashing

-Busy wait, spin lock, deadlocks etc.

-Process schedulers, dispatcher

1: What is the difference between a thread and a process?

Q2: How to processes talk to each other? How can they access the same memory?

Q3: If you have an interrupt section, that when this interrupt happens, you want to wake up  the thread (only then). How do you do that?

Q4: C doesn’t have overriding functions. But, how is that you can add as many args as you want in the function parameters? How does that happen backstage?

 3. What is a semaphore? Explain in detail.

4.What is an interrupt. How does a processor handle an interrupt?

5. What is the exact role of Memory Management Unit?
