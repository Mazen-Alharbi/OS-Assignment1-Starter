# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

process: a heavyweight entity with its own address space.
independent memory space.
expensive to create and manage.

thread: a lightweight entity within a prcoess.
shares address space with other threads in same process.
cheap to create and manage.


---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

if the process doesnt finish within its assigned time quantum, it pause and put it in the end of queue, to make sure others process exucte

Example from my output:
```
 P1 executing quantum [3000ms] 
  ? Quantum progress: [███████████████] 100%
  ? P1 completed quantum 3000ms │ Overall progress: [███████████████████░] 99%
     Remaining time: 25ms
  ? P1 yields CPU for context switch
P1(priority :4)  added to ready queue 
```

**Explanation of example:**
p1 start executing for 3000ms 
and it takes all time quantum 100% but there is 1% remaining to make sure all process execute, paused p1 and add it to the end of queue
---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

new: process is being created and waiting to be admitted to ready queue
runnable: process is ready to execute (Ready state)
running: process is currently exeuting
waiting: process is waiting for an event
terminated: process is finished executed

1. **New**:  Thread thread = new Thread(process); (in method addprocesstoqueue)

2. **Runnable**:  currentThread.start(); (in the while loop)

3. **Running**:  P1 executing quantum (from the output)

4. **Waiting**: currentThread.join(); (in the while loop)
5. **Terminated**:  P1 finished execution! (from the output)

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Tawakkalna app

**Description**: 
when multipe user trying to sign in and scan QR code, the system should respones to users equally and fast 

**Why Round-Robin works well here**: 
fairness: every process gets equal cpu time
good response time for interactive processes
simple to implement

### Example 2: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

---

## Summary

**Key concepts I understood through these questions:**
1. threads and process
2. round-robin
3. ready queue behavior

**Concepts I need to study more:**
1. 
2. 
