---
name: 'Task 4: Implement `cpuEvent)` simulation member method'
about: Task 4 for Students
title: 'Task 4: Implement `cpuEvent()` simulation member method'
labels: enhancement
assignees: ''

---

**Description**

Implement basic `cpuEvent()` CPU cycles.  The `cpuEvent()` is relatively
simple.  The system time should be incremented by 1 every time a CPU event
occurs.  Also, if a process is currently running on the CPU, its `timeUsed`
should be incremented by 1 and its `quantumUsed` as well.  You should use the
`cpuCycle()` member function of the `Process` class to do the work needed to
increment the time used and quantum used of the current running process.

**Suggested Solution**

So the pseudocode for the `cpuEvent()` function is:

```
// increment the system time
systemTime++

// if the cpu is running a process, call the cpuCycle member funciton of the
// process to update its time used and quantum used
if cpu is not idle
  access the process from the processControlBlock
  call the cpuEvent() method on the process that is currently running
```

**Additional Requirements**

- The system time should always be incremented each cpu cycle.
- The time and time quantum is only incremented for a process if a process is currently
  running during this cpu cycle.
