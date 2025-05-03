# Operating System
An operating system (OS) is system software that manages computer hardware, software resources, and provides common services for computer programs. It acts as an intermediary between users and the computer hardware. Operating systems are essential for running applications and managing system resources like memory, processing power, and storage.
## Processes
- **Process:** A process is a program in execution.
- An operating system executes a variety of programs:
  - **Batch system:** Processes jobs in batches without user interaction.
  - **Time-shared system:** Allows multiple users to interact with the system simultaneously.
- A **process** is a program in execution; execution progresses sequentially.

## Process Components
- **Text section** (program code)
- **Program counter & registers** (current activity)
- **Stack** (temporary data: function parameters, return addresses, local variables)
- **Data section** (global variables)
- **Heap** (memory allocated during runtime)

## Process States
1. **New:** Being created.
2. **Running:** Instructions are being executed.
3. **Waiting:** Waiting for an event (e.g., I/O completion).
4. **Ready:** Waiting to be assigned to a processor.
5. **Terminated:** Process has finished execution.

## Process Control Block (PCB)
Contains information such as:
- Process state
- Program counter
- CPU registers
- Memory management information
- Accounting information
- I/O status

## Context Switching
- When an interrupt occurs, the system saves the current process state and loads another process.
- Context-switching is an **overhead** as it does no useful work.

## Process Scheduling
- **Short-term scheduler:** Selects a process for CPU execution.
- **Long-term scheduler:** Controls multiprogramming.
- **Medium-term scheduler:** Swaps processes in and out of memory.
- Queues:
  - **Job queue:** All processes in the system.
  - **Ready queue:** Processes ready to execute.
  - **Device queues:** Processes waiting for I/O.

## Multitasking in Mobile Systems
- **iOS:**
  - One foreground process
  - Limited background processes
- **Android:**
  - Runs foreground & background services independently
  - Uses services to perform background tasks

## Process Creation
- Parent process creates child processes.
- **fork() (Unix):** Creates a new process.
- **exec() (Unix):** Replaces the process’s memory space with a new program.
- **CreateProcess() (Windows):** Creates a new process.

## Process Termination
- **exit() (Unix):** Terminates a process.
- **abort() (Unix):** Parent terminates child process.
- **wait() (Unix):** Parent waits for child process to finish.
- **Orphan & Zombie Processes:**
  - **Orphan:** Parent terminates without waiting for child.
  - **Zombie:** Child terminates but parent does not collect exit status.

## Interprocess Communication (IPC)
### IPC Models:
1. **Shared memory:** Processes communicate via a shared region in memory.
2. **Message passing:** Processes send and receive messages.

### Synchronization:
- **Blocking (Synchronous):**
  - Sender waits for receiver.
  - Receiver waits if no message available.
- **Non-blocking (Asynchronous):**
  - Sender continues execution after sending message.
  - Receiver retrieves a message if available or proceeds without waiting.

### Buffering:
- **Zero capacity:** Sender waits for receiver.
- **Bounded capacity:** Sender waits if queue is full.
- **Unbounded capacity:** Sender never waits.

## Communication in Client-Server Systems
- **Sockets:** Endpoints for network communication.
- **Remote Procedure Calls (RPC):** Abstracts function calls between networked processes.
- **Pipes:** Used for interprocess communication.

## Examples of IPC Systems
- **POSIX:** Uses shared memory segments (`shm_open()`).
- **Mach:** Message-based communication.
- **Windows:** Local Procedure Calls (LPC) for IPC.

---
