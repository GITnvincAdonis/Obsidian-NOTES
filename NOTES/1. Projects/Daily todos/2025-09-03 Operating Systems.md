---
creation date: <% tp.file.creation_date() %>
---

> [!Danger] Concepts
> - Multithreading
> - Process
> - Parts of a Process
> - Thread

### Process
A process is an instance of a computer program. It includes the code for the process, the data it operates and computer resources (etc. RAM)

### Thread
A thread is the single stream of execution of a process

### Multi-Threading
The sharing of CPU processing resources among many threads. The CPU and only process one thread at a time. To `fake` multitasking, the threads are split into time shares and are fed  to the CPU for execution using a scheduling algorythm (FCFS, FCLS, round robin, etc.). 

The slice of a single process is executed by a computer core, and the slice of another thread is queued. This means that a single thread does not monopolize CPU processing time, allowing for the execution of many threads (not necessarily to completion)

Link to original: [[2025-09-03 Skills to learn for SWE]]