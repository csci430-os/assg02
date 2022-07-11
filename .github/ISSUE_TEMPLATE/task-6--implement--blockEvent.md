---
name: 'Task 6: Implement `blockEvent()` member method'
about: Task 6 for Students
title: 'Task 6: Implement `blockEvent()` member method'
labels: enhancement
assignees: ''

---

**Description**

Implement the `blockEvent()` simulation function. The `blockEvent()` function should put the current running process into a BLOCKED state, and should record the `eventId` that the process is now waiting on.  You should use the `block()` `Process` member function in your implementation of `blockEvent()`.

**Suggested Solution**

```
# test for errors first, should be an error if cpu is IDLE when a
# block occurs
if cpu is IDLE
   throw SimulatorException
   

# it is also an error if there is already a process waiting on
# the event that just happened
if blockedList already has a process waiting on this event
   throw SimulatorException
   
# otherwise there is a process running and we can block it on
# the indicated event
Look up the current running process in the processControlBlock and block it
Enter the mapping between the event and this process in the blockedList
Set the cpu to IDLE
```

**Additional Requirements**

- You are required to throw a `SimulatorException` if this method is called when no
  process is currently running on the cpu.
- You are required to throw a `SimulatorException` if there is already a processes
  blocked in the system waiting on the indicated event to occur (simulation does
  not allow more than 1 process to block on any given event).
