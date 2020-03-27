# Description
Design a scheduler that can schedule the processes arriving system at periodical intervals. Every process is assigned with a fixed time slice t milliseconds. If it is not able to complete its execution within the assigned time quantum, then automated timer generates an interrupt. The scheduler will select the next process in the queue and dispatcher dispatches the process to processor for execution. Compute the total time for which processes were in the queue waiting for the processor. Take the input for CPU burst, arrival time and time quantum from the user.
# Explaination:
1)Round Robin is the preemptive process scheduling algorithm.
2)Each process is provided a fix time to execute, it is called a quantum.
3)Once a process is executed for a given time period, it is preempted and other process executes for a given time period.
4)Context switching is used to save states of preempted processes.

Example: Assume there are 5 processes with process ID and burst time given below PID Burst Time P1 6 P2 5 P3 2 P4 3 P5 7 – Time quantum: 2 – Assume that all process arrives at 0. Now, we will calculate average waiting time for these processes to complete. Solution – We can represent execution of above processes using GANTT chart as shown below –

Explanation: – First p1 process is picked from the ready queue and executes for 2 per unit time (time slice = 2). If arrival time is not available, it behaves like FCFS with time slice. – After P2 is executed for 2 per unit time, P3 is picked up from the ready queue. Since P3 burst time is 2 so it will finish the process execution at once. – Like P1 & P2 process execution, P4 and p5 will execute 2 time slices and then again it will start from P1 same as above. Waiting time = Turn Around Time – Burst Time P1 = 19 – 6 = 13 P2 = 20 – 5 = 15 P3 = 6 – 2 = 4 P4 = 15 – 3 = 12 P5 = 23 – 7 = 16 Average waiting time = (13+15+4+12+16) / 5 = 12
