---
name: 'Task 1: Implement `ProcessSimulator` accessor and getter methods'
about: Task 1 for Students
title: 'Task 1: Implement `ProcessSimulator` accessor and getter methods'
labels: enhancement, good first issue
assignees: ''

---

**Description**

Implement the following missing getter and accessor methods:

- class constructor, initialize the `timeSliceQuantum` as given.  Initialize all other
  member variables as appropriate and as seen in the tests for the initial state of
  the simulation.
- `getTimeSliceQuantum()`
- `getNextProcessId()`
- `getSystemTime()`
- `getNumActiveProcesses()`
- `getNumFinishedProcesses()`
- `readyQueueSize()`
- `readyQueueFront()`
- `readyQueueBack()`


**Suggested Solution**


**Additional Requirements**

- You are required to correctly modify the `ProcessSimulator` class constructor to
  intialize the time slice quantum for a simulation as indicated, and initialize all
  other member variables to 0 or their initial value before the simulation starts.
- You are required to use the `processControlBlock` map to hold the actual process
  instances of the simulation.
- You are required to use the `readyQueue` STL list to hold a queue of process identifiers
  that are ready and waiting for the cpu.
- You are required to use the `cpu` member variable to keep track of the process id of
  the current running process (or IDLE when no process is running).
