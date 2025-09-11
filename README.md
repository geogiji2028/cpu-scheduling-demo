# cpu-scheduling-demo

1. Shortest Job First (SJF)

Definition: In this scheduling, the process with the shortest burst time (execution time) is executed first.

Type: Can be non-preemptive (once a process starts, it runs till completion) or preemptive (called Shortest Remaining Time First – SRTF).

Advantage: Minimizes average waiting time, making it optimal in many cases.

Disadvantage: Requires knowledge of burst time in advance (which is often difficult). It may also cause starvation for longer processes.

Use case: Suitable when burst times are predictable, e.g., batch systems.

2. First Come First Serve (FCFS)

Definition: The process that arrives first in the ready queue is executed first. It works like a queue (FIFO – First In, First Out).

Type: Non-preemptive.

Advantage: Simple to implement and fair (no process is skipped).

Disadvantage: Can lead to convoy effect (a long process delays all others behind it). Average waiting time can be high if burst times vary a lot.

Use case: Good for batch processing where tasks arrive in order and must finish sequentially.

3. Round Robin (RR)

Definition: Each process is assigned a fixed time quantum (time slice). Processes are executed in a circular order. If a process isn’t finished within its time quantum, it is put back at the end of the queue.

Type: Preemptive.

Advantage: Provides fair CPU allocation, good for time-sharing systems. Reduces starvation since every process gets CPU regularly.

Disadvantage: Performance depends on choosing the right time quantum. Too small → more context switching (overhead). Too large → behaves like FCFS.

Use case: Ideal for interactive systems where response time is important (e.g., multi-user OS).
