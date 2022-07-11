---
name: 'Task 2: Implement `newEvent()`  member function'
about: Task 2 for Students
title: 'Task 2: Implement `newEvent()` member function'
labels: enhancement
assignees: ''

---

**Description**

Implement the `newEvent()` function.  The `newEvent()` function is called
whenever a "new"  occurs in the simulation.  Basically you need to create a new
process, assign it the correct next process id, make the process ready, and add
it to the end of your ready queue.

Also as part of this task you need to implement the `getProcess()` accessor method.
This method is used mainly for testing.  It should return a reference to the `Process`
instances for the given `Pid`.

**Suggested Solution**


**Additional Requirements**

- You are required to use the `processControlBlock` map as given for the implementaiton
  of creating new processes in the simulation, and as the mechanism to return references
  to these process instances for testing.

