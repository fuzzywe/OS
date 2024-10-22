[9/27, 6:11 AM] Ruthika: What is cache? Choosing which loop increases cache performance.
Given the following. Modify the code such that first thread A prints A and then thread B prints B.
(Concept of semaphores)
[9/27, 6:12 AM] Ruthika: What is the OS? What are the various functions of OS?
    Difference between Multiprogramming, Time-Sharing, and Multi-Processing.
    https://www.geeksforgeeks.org/difference-between-multitasking-multithreading-and-multiprocessing/
    Difference between Single Core and Multicore Processor.
    Difference between CPU and GPU. https://www.geeksforgeeks.org/difference-between-cpu-and-gpu/
    What is Multilevel Queue Scheduling? How it is different from Priority Scheduling.
    Given Arrival Time, Burst time of Processes. Draw its Gantt chart by Preemptive SJF.
    What is multithreading? Is multithreading useful for uniprocessor?
    Compare Thread Switching and Process Switching. Which one is fast?
    What are Semaphores? Give an example by using semaphore such that it ensures mutual exclusion property of critical section?
    What are Wait and Signal? Write their implementation. https://www.geeksforgeeks.org/semaphores-in-process-synchronization/
    What is Memory Management Unit?
    Explain one level paging with a diagram?
    What is the difference between the Logical Address and Physical Address? Why there is a need for a logical address?
    Given Page Size, No of bits in Logical and Physical Address space. Find the total no of pages and frames?
    What is the difference between User mode and Kernel Mode? How they are switched to each other?
    What is a System Call? Why it is required?
    Difference between Kernel Level and User Level thread? https://www.geeksforgeeks.org/difference-between-user-level-thread-and-kernel-level-thread/
    Difference between RAM and ROM. Why RAM is Called Random Access Memory?
[9/27, 6:17 AM] Ruthika: How stack works in recursion 
Implement in-order traversal using stack and optimize it and explain time and space complexity.
Write a C program for handling 32-bit multiplication on a microprocessor ALU supporting 16-bit multiplication
[9/27, 6:19 AM] Ruthika: What is the difference between SSD and HDD?
Types of SSD?
Tell me CPU parts.
How computer boots, bios?
What is blod, and how did it has occurred?
Which games you played did yed what game settings you change (FPS, resolution)
How to disable/enable storage devices from bios?
How to block any service or app at startup
[9/27, 6:19 AM] Ruthika: Explain how computer memory works.
    How does information travel from Secondary Memory to CPU Registers.
    What is cache memory?
    What are L1, L2, L3 caches?

    He also asked me questions on GPU architecture and CUDA programming since I had a CUDA project on my resume.

    Explain the difference in CPU and GPU architecture?
    How do we manipulate memory in CUDA?
[9/27, 7:33 AM] Ruthika: Here’s a clear differentiation between CPU and GPU architecture:

| Feature                | CPU (Central Processing Unit)                     | GPU (Graphics Processing Unit)                       |
|------------------------|----------------------------------------------------|-----------------------------------------------------|
| Core Count             | Few powerful cores (4-16 typically)                | Many smaller, simpler cores (hundreds to thousands) |
| Task Type              | Optimized for sequential, general-purpose tasks    | Optimized for parallel, repetitive tasks (e.g., graphics, AI) |
| Latency                | Low-latency, fast task switching                   | Higher latency, better for sustained workloads      |
| Clock Speed            | Higher clock speed per core                        | Lower clock speed but more cores in parallel        |
| Flexibility            | More flexible for a wide range of tasks            | Specialized for specific, parallel tasks like matrix calculations |
| Cache                  | Larger cache per core to speed up access to memory | Smaller cache, focuses on throughput rather than low-latency access |
| Power Efficiency       | Generally less power-efficient for parallel tasks  | More power-efficient for parallel workloads         |

CPU excels at handling general, diverse tasks, while GPUs are ideal for parallel computations like 3D rendering or AI workloads.
[9/27, 7:39 AM] Janani: ache is necessary because it is much faster than RAM.
CPU caches provide high-speed access to frequently used data, significantly reducing latency and preventing the CPU from being idle while waiting for slower memory.
Even with large amounts of RAM, without cache, modern CPUs would be underutilized and overall performance would be much lower.
[9/27, 7:46 AM] Janani: Cache memory is a type of temporary memory that stores frequently accessed data for faster access by the central processing unit (CPU). It's a vital component of computer systems that helps improve performance.
[9/27, 7:47 AM] Janani: Cache memory acts as a buffer between the CPU and the main memory to ensure faster data access, improving overall system performance.
[9/27, 8:18 AM] Ruthika: L1 Cache:located on the CPU core, providing immediate access to frequently used data and instructions.
[9/27, 8:20 AM] Janani: L1 cache
The fastest and smallest cache, located directly in the CPU. It's also known as the primary cache. L1 cache is typically divided into two parts: L1i, which stores instructions, and L1d, which stores data. 
L2 cache
Often larger than L1, but slower. It can be located on the processor chip or on a separate chip connected to the CPU by a high-speed bus. 
L3 cache
The largest cache, but also the slowest. It's located on the computer that uses the L2 cache. L3 cache is designed to improve the performance of L1 and L2
[9/27, 8:48 AM] Janani: Volatility:

RAM: Volatile (loses data when powered off).
Secondary Memory: Non-volatile (retains data).
Speed:

RAM: Fast access speeds, suitable for active processes.
Secondary Memory: Slower access speeds, used for long-term storage.
Structure:

RAM: Organized in addressable memory cells.
Secondary Memory: Organized in files, sectors, and blocks.
[9/27, 10:00 AM] Ruthika: https://computer.howstuffworks.com/ram.htm
[9/27, 10:24 AM] Ruthika: Is flash memory same as RAM?
No, flash memory is not the same as RAM. RAM is volatile and only stores data while the power is on, while flash memory is non-volatile and stores data even when the power is off.
What do you mean flash memory?
Flash memory is also known as flash storage. Flash memory is a type of non-volatile memory that can be erased and reprogrammed.
[9/27, 11:23 AM] Ruthika: BIOS (Basic Input/Output System) initializes and runs POST to check hardware components (CPU, RAM, disk drives) for errors.
[9/27, 11:24 AM] Ruthika: The computer loads the basic input/output system (BIOS) from ROM. The BIOS provides the most basic information about storage devices, boot sequence, security, Plug and Play (auto device recognition) capability and a few other items.
[9/27, 12:02 PM] Ruthika: In-Depth Explanation of User-Level Threads (ULTs) and Kernel-Level Threads (KLTs) with Real-Life Programming Examples:
1. User-Level Threads (ULTs) - Example: Temple Run Game

In a game like Temple Run, several tasks must run simultaneously:

    Updating the character’s position.
    Rendering the game graphics.
    Detecting player input (e.g., swipes or taps).
    Updating the score and game state.

Here’s how User-Level Threads (ULTs) work in this context:

    Game-Managed Multitasking: The game handles these tasks itself using a thread library within the user space (outside the OS kernel). For example, there could be one thread for graphics, another for player input, and another for score calculation. All these threads are managed entirely by the game, without involving the operating system's kernel.

    Thread Scheduling: The game engine decides when to run each thread. It might switch from processing the player’s movement to rendering a new game frame, based on internal logic. This scheduling is fast because it doesn't require the overhead of going through the operating system.

    Limitations: If one thread encounters a blocking operation, such as a file read or a long calculation, the whole game could pause. Since the OS kernel doesn’t know that multiple threads exist, it treats the entire game as a single process. If one thread is stuck, the entire process can get stuck because the OS can’t schedule other threads of the game independently.

Analogy:

Imagine you're managing multiple tasks (character movement, rendering, etc.) yourself, without help from the system. You can switch quickly between tasks because there’s no external manager, but if one task gets stuck, everything stops until that task is resolved.
2. Kernel-Level Threads (KLTs) - Example: Web Server (Apache)

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

Summary:

    ULTs (Temple Run Example): The game manages threads without involving the OS. It's fast but limited in handling blocking operations.
    KLTs (Apache Web Server Example): The operating system manages threads. It’s slightly slower due to kernel involvement, but offers better concurrency, especially when tasks (like web requests) are blocking.

These differences dictate the choice of threading model based on the needs of the application—performance vs. concurrency.
