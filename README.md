# CPU Scheduling Algorithms in C++

This project provides an implementation of several CPU scheduling algorithms using C++. The algorithms included are First Come First Serve (FCFS), Round Robin (RR), Shortest Process Next (SPN), Shortest Remaining Time (SRT), Highest Response Ratio Next (HRRN), Feedback (FB), and Aging.

## Table of Contents
- [Overview](#overview)
- [Scheduling Algorithms](#scheduling-algorithms)
  - [First Come First Serve (FCFS)](#first-come-first-serve-fcfs)
  - [Round Robin with Variable Quantum (RR)](#round-robin-with-variable-quantum-rr)
  - [Shortest Process Next (SPN)](#shortest-process-next-spn)
  - [Shortest Remaining Time (SRT)](#shortest-remaining-time-srt)
  - [Highest Response Ratio Next (HRRN)](#highest-response-ratio-next-hrrn)
  - [Feedback (FB)](#feedback-fb)
  - [Feedback with Variable Quantum (FBV)](#feedback-with-variable-quantum-fbv)
  - [Aging](#aging)
- [Setup Instructions](#setup-instructions)
- [Input Format](#input-format)
- [Contributors](#contributors)

## Overview

This repository contains implementations of various CPU scheduling algorithms, each designed to manage process execution in different ways to optimize performance and efficiency.

## Scheduling Algorithms

### First Come First Serve (FCFS)

The FCFS algorithm schedules processes in the order they arrive. It's straightforward but can suffer from the convoy effect if a lengthy process arrives before shorter ones. FCFS is a non-preemptive algorithm, meaning once a process starts, it runs to completion.

### Round Robin with Variable Quantum (RR)

Round Robin (RR) with a variable time quantum is a time-sharing scheduling algorithm. The quantum can be adjusted based on process requirements, with shorter processes receiving smaller quanta. This method helps balance CPU time efficiently among processes.

### Shortest Process Next (SPN)

SPN schedules processes based on the shortest burst time first. It is a non-preemptive algorithm, where the process with the shortest execution time is always selected next. This can minimize average waiting time but may lead to longer processes being delayed.

### Shortest Remaining Time (SRT)

SRT is the preemptive counterpart to SPN. It selects the process with the shortest remaining time to execute next. If a new process arrives with a shorter remaining time, it preempts the current process. This approach helps reduce waiting time for shorter processes.

### Highest Response Ratio Next (HRRN)

HRRN prioritizes processes based on their response ratio, calculated as (waiting time + burst time) / burst time. This non-preemptive algorithm ensures processes with longer waiting times are given higher priority, balancing fairness and efficiency.

### Feedback (FB)

Feedback scheduling uses multiple priority queues, dynamically adjusting process priorities. Higher priority processes are executed first, and as they run, they are moved to lower priority queues. This method handles a mix of short and long processes effectively.

### Feedback with Variable Quantum (FBV)

FBV extends the Feedback algorithm by varying the time quantum across priority levels. This variation allows the algorithm to allocate more CPU time to higher-priority processes and less to lower-priority ones, improving overall efficiency.

### Aging

The Aging algorithm addresses process starvation by gradually increasing the priority of waiting processes. Each time the scheduler runs, it increments the priority of all ready processes, ensuring that no process waits indefinitely.

## Setup Instructions

1. Clone this repository to your local machine.
2. Ensure you have `g++` and `make` installed on your system.
   ```bash
   sudo apt-get install g++ make
