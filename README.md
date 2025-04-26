
# CPU Scheduling Simulation with Deadlock Detection and Recovery

## Overview

This project simulates a CPU scheduling system that incorporates **priority scheduling with round-robin**, **deadlock detection**, and **deadlock recovery** mechanisms.  
It models a single-core CPU, multiple processes, and multiple resources (each resource has only one instance).

✅ **Features:**
- Priority scheduling with round-robin within the same priority level.  
- Deadlock detection using a graph-based cycle detection algorithm.  
- Deadlock recovery by terminating a process and reclaiming its resources.  
- I/O operations simulation: processes enter I/O queue and rejoin the ready queue after I/O completion.  
- Displays Gantt chart for visualization.  
- Reports average waiting time and turnaround time for all processes.

---

## Files

| File | Description |
|:-----|:------------|
| `Main.py` | Main source code implementing CPU scheduling, deadlock detection, and recovery |
| `input.txt` | Input file specifying processes, arrival times, priorities, and bursts |
| `Test_Cases.pdf` | Test case descriptions for project validation |
| `Project_Description.pdf` | Full project description and requirements |

---

## Input Format

Each process is described in a single line in the `input.txt` file:

```
[PID] [Arrival Time] [Priority] | CPU{...}, IO{...}, CPU{...}
```

**Example:**

```
0 0 0 | CPU{R[1], 20, R[2], 4, F[1], F[2]}
1 0 0 | CPU{R[2], 6, R[3], 3, F[2], F[3]}
2 0 0 | CPU{R[3], 6, R[1], 3, F[1], F[3]}
```

- `R[x]`: Request resource x.
- `F[x]`: Free resource x.
- CPU/IO bursts are given in sequence.

---


## Output

- Console logs showing process execution steps, resource allocations, deadlock detections, and recovery actions.
- Gantt Chart visualization displaying the execution timeline.
- Average Waiting Time and Average Turnaround Time printed at the end.


