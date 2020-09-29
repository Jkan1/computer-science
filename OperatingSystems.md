
-  **Scheduling types**

-  **Mutex & Semaphore -** are kernel resources that provide synchronization services (also called as synchronization primitives)

-   **Critical Section** - concurrent accesses to shared resources can lead to unexpected or erroneous behavior, so parts of the program where the shared resource is accessed need to be protected in ways that avoid the concurrent access. This protected section is the critical section or critical region

-   **Race Condition** is a situation that may occur inside a critical section. This happens when the result of multiple thread execution in critical section differs according to the order in which the threads execute

-   **Semaphore** is simply a variable, a signalling mechanism, and a thread that is waiting on a semaphore can be signalled by another thread. It uses two atomic operations, 1)wait, and 2) signal for the process synchronisation

-   **Child Process** - created as its parent process's copy and inherits most of its attributes. If a child process has no parent process, it was created directly by the kernel. If a child process exits or is interrupted, then a SIGCHLD signal is send to the parent process

-   **Fork** - fork is an operation whereby a process creates a copy of itself. Fork is the primary method of process creation on Unix-like operating systems.

-   **Thread Control Block** - Modern operating systems allow a process to be divided into multiple threads of execution, which share all process management information except for information directly related to execution. This information is held in a thread control block (TCB).

-   **Context Switching** is the process of storing the state of a process or thread, so that it can be restored and resume execution at a later point. This allows multiple processes to share a single central processing unit, and is an essential feature of a multitasking operating system

-   **Kernel**

-   **Thread** -  smallest sequence of programmed instructions that can be managed independently by a scheduler, which is typically a part of the operating system

-   **Process Control Block(PCB)** - management info about process -

-   **Process** - program under execution job- instance of program Execution - This means, for example, that if you open up two browser windows then you have two processes, even though they are running the same program

-   **Address Space** - There is one address space for the whole process. Each thread has its own stack and registers, but all threads' stacks are visible in the shared address space. If one thread allocates some object on its stack, and sends the address to another thread, they'll both have equal access to that object

-   **Job** - group of tasks - what to be done- passed on from scheduler to os

-   **Task** - unit of execution

-   **Interrupt & Trap Signals**