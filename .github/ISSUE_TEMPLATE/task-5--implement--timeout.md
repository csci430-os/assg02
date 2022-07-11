---
name: 'Task 5: Implement `timeout()` simulation member method'
about: Task 5 for Students
title: 'Task 5: Implement `timeout()` simulation member method'
labels: enhancement
assignees: ''

---

**Description**

Implement the `timeout()` function.  This is the other implicit action needed
for your simulation.  The basic thing that `timeout()` should do is to test if
the quantumUsed of the current running process is equal to or has exceeded the
system time slice quantum.  If it has, then the process needs to be timed out,
which means it goes back to a ready state and is returned back to the tail of
the ready queue.

**Suggested Solution**

The pseudocode for the `timeout()` function is:

```
// if cpu is idle, no process to check currently
if cpu is idle
    return
	
// otherwise check the current running process
look up running process in the processControlBlock
if process time slice quantum is exceeded:
   timeout the process
   put the process on the back of the ready queue
   set the cpu to IDLE
```


**Additional Requirements**

- You are required to silently return when the cpu is IDLE as in that case no process is currently running so nothing can be timed out.
- You are required to use the `isQuantumExceeded()` and `timeout()` member methods of the `Process` class/instance in the implementation of the simulations timeout procedure.

