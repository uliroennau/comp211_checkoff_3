# COMP 211 Checkoff 3

Exploration of Multilevel Feedback Queues using AI as a tool for learning.

## What is MLFQ?

A CPU core can only run a single program at a time, so the OS scheduler must decide what ready program runs when. There are many proposed solutions for this, including First-Come, First Served, Shortest Job First, and Round-Robin (see presentation for more info), but MLFQ is a solution to this problem that solves the shortcomings of simpler proposals by watching what each ready job done in the past:

- There are several priority levels, and every job starts at the top one.
- If a job uses up its CPU time, it moves down a level.
- Higher levels run first, and jobs on the same level take turns.
- Every so often, all jobs are pushed back to the top.

The result gets close to Shortest Job First's turnaround time and Round-Robin's response time.

# What I explored

- How CPUs switch between programs and from running, ready, and blocked states.
- The two main metrics: **response time** and **turnaround time**.
- First-Come First-Served, Shortest Job First, and Round-Robin, and what each one still lacks.
- MLFQ's first-draft rules, the scenarios that break them, and why they need to be updated.

# Interesting Discoveries

- **Run time != turnaround time.** A job can technically only need 10ms, but may take 120ms under First-Come, First Served if it must wait on slower programs before it.
- **The rules can be gamed.** Under the first-draft rules, if a program uses 9ms of its 10ms slice and then does a quick request (e.g. I/O), it keeps top priority and can get 90% of the CPU against a job below it.

# Sources
- Arpaci-Dusseau and Arpaci-Dusseau, *Operating Systems: Three Easy Pieces*, Chapter 8 ([ostep.org]((https://pages.cs.wisc.edu/~remzi/OSTEP/)))
- Guided conversation with Claude checked against OSTEP
