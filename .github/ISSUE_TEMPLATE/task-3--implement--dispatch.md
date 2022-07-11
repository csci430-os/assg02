---
name: 'Task 3: Implement `dispatch()`  member method'
about: Task 3 for Students
title: 'Task 3: Implement `dispatch()` member method'
labels: enhancement
assignees: ''

---

**Description**

First implement the `isCpuIdle()` and `runningProcess()` member functions.  You
need to create these functions and add them to the header and implementation files.
These functions will use the `cpu` member variable to do their work.

Implement the `dispatch()` member function.  The purpose of the dispatch is
to check if the cpu is currently idle, and if it is, it should dispatch the
next process that is at the head of the ready queue.  It can be the case that
the ready queue is empty, and thus in that case `dispatch()` would do nothing
since no process is currently ready to be dispatched, and the cpu would still be
idle after returning from the failed dispatch.

**Suggested Solution**

The pseudocode of `dispatch()` looks something like the following:

```
// first check if something is currently running, we only dispatch
// something new when cpu is not currently running anything
if cpu is not idle:
   do nothing

// otherwise cpu is idle, so try and dispatch a process, but if
// ready queue is empty, we still can't dispatch the next process
if ready queue is empty:
   do nothing
   
// otherwise cpu is idle and there is one or more process ready to run,
// so get the process at front of queue and make it the running process
pid = ready queue front process
cpu = pid
look up process in the processControlBlock and put it in the running state
```


**Additional Requirements**

- You are required to quietly do nothing if there is currently a process is running.
  In that case we are not ready to dispatch yet.
- But also, if the cpu is IDLE but there are no processes ready to run on the ready queue,
  again we are not ready to dispatch so this function quitely does nothing.

