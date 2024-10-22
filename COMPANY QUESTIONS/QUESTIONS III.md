[9/25, 11:10 PM] Ruthika: 35. What is the Firewall?
A firewall is a network security device, either hardware or software-based, which monitors all incoming and outgoing traffic and based on a defined set of security rules it accepts, rejects or drops that specific traffic
[9/25, 11:10 PM] Ruthika: 34. What is Fragmentation
The process of dividing a computer file, such as a data file or an executable program file, into fragments that are stored in different parts of a computer’s storage medium, such as its hard disc or RAM, is known as fragmentation in computing.
[9/25, 11:35 PM] Ruthika: 3. How many processors and cores and sub processes running how to find out using application (in windows) , using command (in linux)
Here I answered Ill use Windows task manager to find out but she said they show us the main processes and she wants to see all the sub processes too
[9/25, 11:36 PM] Ruthika: What does loader and linker do and in which part of memory everything is stored
[9/26, 3:20 AM] Janani: https://leetcode.com/problems/lru-cache/description/
[9/26, 3:51 AM] Ruthika: In CV, you have written that you improved slow loading of application. how did you do that?
How will you improve it for a mobile application?
How to improve API response time / optimise the APIs ?
How to make database queries faster or optimise the queries?
How do you choose sharding key ? What are the factors considered for sharding the table into multiple shards ?
Difference between Horizontal Sharding vs Horizontal Partitioning?
What is horizontal Partitioning ?
Difference between partitioning and sharding?
[9/26, 3:52 AM] Ruthika: How will you design Amazon’s database architecture in terms of sharding and partitioning ? How will you make sure locking while writing in a heavily read extensive environment ? — I explained Master slave, master master slave with multiple shards but He wasn’t satisfied.
Asked for which version of java are you comfortable with ? I replied java 8.
What is lambda ? How does it improve/help in implementation ?
What difference does lambda make in memory and processing from JVM perspective?
What is functional interface ? Some examples of functional interface?
Difference between Synchronized Hashmap, ConcurrentHashmap, Hashmap?
In last, Asked a DS question: Given a string in format aabbbcccaaa, encode this in shorter format i.e. a2b3c3a3
[9/26, 9:06 AM] Janani: https://www.ibm.com/topics/virtualization
[9/26, 10:01 AM] Ruthika: To view all processes, including subprocesses, on Windows and Linux, you can use the following methods:

### **On Windows:**
1. **Windows Task Manager**:
   - You can use **Task Manager** to see the main processes and subprocesses, but Task Manager groups them in a hierarchical format (tree view). To view subprocesses:
     - Right-click on the **Taskbar** and select **Task Manager**.
     - Click **Details** or **Processes** tab.
     - Right-click on the column headers, select **"Select Columns"**, and check **"PID"** (Process ID) and **"Command Line"**. This will help you see which subprocesses belong to which main process.

2. **Using PowerShell**:
   - You can use PowerShell to view all processes and their subprocesses.
     ```powershell
     Get-Process | Format-Table -Property Id, ProcessName, ParentId
     ```
   - This will show the **process ID (PID)** and the **Parent Process ID (PPID)**, indicating which process is a subprocess of another.

3. **Using Sysinternals Process Explorer** (More Advanced):
   - **Process Explorer** is a more detailed tool for viewing processes and subprocesses.
     - Download it from the [Sysinternals website](https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer).
     - It shows the entire process tree, allowing you to see both parent processes and their subprocesses.

### **On Linux**:
1. **Using `ps` Command**:
   - To see all processes and subprocesses, you can use the `ps` command with flags to view the process tree:
     ```bash
     ps -ef --forest
     ```
   - The `--forest` option shows a tree-like structure, making it easier to see which processes are parent and which are child processes.

2. **Using `htop` Command** (Interactive):
   - **htop** is an interactive process viewer that shows a real-time list of processes and subprocesses.
     - You may need to install it first:
       ```bash
       sudo apt install htop
       ```
     - Run the command:
       ```bash
       htop
       ```
     - In `htop`, you can press **F5** to toggle the **tree view** and see the hierarchy of processes and their subprocesses.

3. **Using `pstree` Command**:
   - You can use `pstree` to display processes in a tree format.
     ```bash
     pstree -p
     ```
   - The `-p` option shows the process IDs along with the tree structure.

These methods will give a detailed view of processes and their subprocesses both on Windows and Linux.

2. What is the OS? What are the various functions of OS?
An Operating System acts as a communication bridge (interface) between the user and computer hardware.
Functions of an Operating System

    Memory Management: The operating system manages the Primary Memory or Main Memory. Main memory is made up of a large array of bytes or words where each byte or word is assigned a certain address
    Processor Management: In a multi-programming environment, the OS decides the order in which processes have access to the processor, and how much processing time each process has.
    Device Management: An OS manages device communication via its respective drivers. It performs the following activities for device management.
    File Management: A file system is organized into directories for efficient or easy navigation and usage. These directories may contain other directories and other files. An Operating System carries out the following file management activities.
    User Interface or Command Interpreter: The user interacts with the computer system through the operating system. Hence OS acts as an interface between the user and the computer hardware

What do you  know in OS.
4.   What is process, thread? Difference Between process and thread.
https://www.geeksforgeeks.org/operarting-system-thread/
5.   What resources does a process use?How does the process   
   resources information is maintained?https://www.geeksforgeeks.org/operating-system-process-table-process-control-block-pcb/

6.   What resources do threads use?https://www.geeksforgeeks.org/operarting-system-thread/
7.   What should we do if we do not want to share a file among threads?

8.   What are locks?https://www.geeksforgeeks.org/lock-variable-synchronization-mechanism/
9.   What is mutex ?What is semaphore? Difference between them.
https://www.geeksforgeeks.org/mutex-vs-semaphore/

10.Mutex vs Binary semaphore? Are they logically equivalent ?https://stackoverflow.com/questions/62814/difference-between-binary-semaphore-and-mutex

11.What is virtual memory  and why do we use it?https://www.geeksforgeeks.org/virtual-memory-operating-systems/

12.What is demand paging? How to map logical to physical address?https://www.geeksforgeeks.org/virtual-memory-operating-systems/
13.Which address is known to CPU?

14.What  is volatile keyword? Why do we need it?https://www.geeksforgeeks.org/understanding-volatile-qualifier-c-set-1-introduction/https://www.geeksforgeeks.org/understanding-volatile-qualifier-in-c/

15.What is static variable ?Show by example.https://www.geeksforgeeks.org/static-variables-in-c/
16.Where does static variable get stored?https://www.geeksforgeeks.org/memory-layout-of-c-program/

   
